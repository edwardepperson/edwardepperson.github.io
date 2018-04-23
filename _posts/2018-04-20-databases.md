---
layout: default
permalink: databases-revisited
---

The artifact that I decided to revisit for the database portion of the final project is a course provided database for the database MongoDB. It is a simple database that contains research records for a series of various companies. The inclusion of this artifact is intended to signal to potential employers and peers that I am capable of working with and improving a database that someone else created. A major portion of software development is maintaining some legacy code and preparing for future changes or modifications. It also showcases my abilities within a popular database system for web development applications.
	I analyzed the original schema and picked apart much of the data types present in the research documents. Using the following code, var col_list = db.research.findOne();, I was able to obtain a basic list of columns from the table consisting of:
_id	providerships
name	total_money_raised
permalink	funding_rounds
crunchbase_url	investments
homepage_url	acquisition
blog_url	acquisitions
blog_feed_url	offices
twitter_username	milestones
category_code	video_embeds
number_of_employees	screenshots
founded_year	external_links
deadpooled_year	partners 
tag_list	
alias_list	
email_address	
phone_number	
description	
created_at	
updated_at	
overview	
image	
products	
relationships	
competitions	
With this information in hand I normalized the data and reduced the number of fields. Instead of fields with the postfix _url I decide to normalize those fields into a single identifier links_id which links to a separate table containing links that relate to the research document. 
	When normalizing the companies database, I found myself constantly questioning what would be a proper restructuring of a document that lacks a schema. MongoDB brings extreme flexibility with it, so much so that it is, simultaneously, daunting and liberating to quickly alter a table’s structure. It speaks to the power that a NoSQL database brings to the table when considering what to use for development purposes. 
