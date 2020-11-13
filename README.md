Contacts Restful API using cakephp :

Routing : 

List : /api/contacts.json [GET]
GET by id : /api/contacts/{{ID}}.json  [GET]
Add : /api/contacts.json  [POST]
Update By Id : /api/contacts/{{ID}}.json [PUT]
Delete By Id : /api/contacts/{{ID}}.json [DELETE]

MySQL Database : 

CREATE TABLE IF NOT EXISTS `contacts` (
  `id` int(6) unsigned NOT NULL,
  `first_name` varchar(200) NOT NULL,
  `last_name` varchar(200) NOT NULL,
  `phone_number` varchar(20) NOT NULL,
  `address` varchar(200) NOT NULL,
  `company_id` int(6) unsigned NULL,
  `notes` varchar(200) NOT NULL,
  `add_notes` text NOT NULL,
  `internal_notes` text NOT NULL,
  `comments` text NOT NULL,
  PRIMARY KEY (`id`)
) DEFAULT CHARSET=utf8;


CREATE TABLE IF NOT EXISTS `companies` (
  `id` int(6) unsigned NOT NULL,
  `company_name` varchar(200) NOT NULL,
  `phone_number` varchar(20) NOT NULL,
  `address` varchar(200) NOT NULL,
  `notes` varchar(200) NOT NULL,
  `add_notes` text NOT NULL,
  `internal_notes` text NOT NULL,
  `comments` text NOT NULL,
  PRIMARY KEY (`id`)
) DEFAULT CHARSET=utf8;
