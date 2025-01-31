1. Search Operators
()
Group multiple terms or operators (advanced expressions).

Syntax: (<term> or <operator>)
Example: inurl:(html | php)
*
Wildcard operator that matches any word.

Syntax: <text> * <text>
Example: How to * a computer
""
Exact match (case-insensitive).

Syntax: "<keywords>"
Example: "google"
m..n / m...n
Search for a range of numbers (n must be greater than m).

Syntax: <number>..<number>
Example: 1..100
-
Excludes documents that match the operator (NOT operator).

Syntax: -<operator>
Example: -site:youtube.com
+
Include documents that match the operator.

Syntax: +<operator>
Example: +site:youtube.com
|
Logical OR operator; only one of the options needs to match.

Syntax: <operator> | <operator>
Example: "google" | "yahoo"
~
Search for synonyms of the given word (note: not supported by Google anymore).

Syntax: ~<word>
Example: ~book
@
Perform a search on the given social media platform (better to use site:).

Syntax: @<socialmedia>
Example: @instagram
after
Find documents published or indexed after a given date.

Syntax: after:<yy(-mm-dd)>
Example: after:2020-06-03
allintitle
Same as intitle but allows multiple keywords (separated by space).

Syntax: allintitle:<keywords>
Example: allintitle:dog cat
allinurl
Same as inurl but allows multiple keywords (separated by space).

Syntax: allinurl:<keywords>
Example: allinurl:search com
allintext
Same as intext but allows multiple keywords (separated by space).

Syntax: allintext:<keywords>
Example: allintext:math science university
AROUND
Search for documents where two words appear within n words of each other.

Syntax: <word1> AROUND(<n>) <word2>
Example: google AROUND(10) good
author
Search for articles written by a specific author.

Syntax: author:<name>
Example: author:Max
before
Find documents published or indexed before a given date.

Syntax: before:<yy(-mm-dd)>
Example: before:2020-06-03
cache
Search on the cached version of a website using Google’s cache.

Syntax: cache:<domain>
Example: cache:google.com
contains
Search for documents that link to a specific file type (not supported by Google).

Syntax: contains:<filetype>
Example: contains:pdf
date
Find documents published within the past n months (not supported by Google).

Syntax: date:<number>
Example: date:3
define
Look up definitions for a given word or phrase.

Syntax: define:<word>
Example: define:funny
ext
Search for a specific file type (alias for filetype).

Syntax: ext:<documenttype>
Example: ext:pdf
filetype
Restrict results to a given file type.

Syntax: filetype:<documenttype>
Example: filetype:pdf
inanchor
Search for a keyword within the anchor text of links.

Syntax: inanchor:<keyword>
Example: inanchor:security
index of
Look for directory listings (often exposes direct downloads).

Syntax: index of:<term>
Example: index of:mp4 videos
info
Retrieve information about a website from Google’s cache and related data.

Syntax: info:<domain>
Example: info:google.com
intext
Force the given keyword to appear in the document’s text.

Syntax: intext:<keyword>
Example: intext:news
intitle
Force the given keyword to appear in the title of the document.

Syntax: intitle:<keyword>
Example: intitle:money
inurl
Force the given keyword to appear in the URL of the document.

Syntax: inurl:<keyword>
Example: inurl:sheet
link / links
Find documents whose links contain the given keyword (useful for backlinks).

Syntax: link:<keyword>
Example: link:google
location
Filter documents based on location.

Syntax: location:<location>
Example: location:USA
numrange
Search within a numeric range (similar to m..n).

Syntax: numrange:<number>-<number>
Example: numrange:1-100
OR
Alias for the | operator.

Syntax: <operator> OR <operator>
Example: "google" OR "yahoo"
phonebook
Find related phone numbers associated with a given name.

Syntax: phonebook:<name>
Example: phonebook:"william smith"
relate / related
Find pages related to a specific website.

Syntax: relate:<domain>
Example: relate:google.com
safesearch
Exclude adult or explicit content from results.

Syntax: safesearch:<keyword>
Example: safesearch:sex
source
Search within a specific news source (though using site: is generally preferred).

Syntax: source:<news>
Example: source:theguardian
site
Restrict search results to a specific website or TLD.

Syntax: site:<domain>
Example: site:google.com
stock
Search for stock market information.

Syntax: stock:<stock>
Example: stock:dax
weather
Retrieve weather information for a location.

Syntax: weather:<location>
Example: weather:Miami
2. General Google Dorks
intitle:"Index of"
intitle:"Index of" site:example.com
filetype:log inurl:"access.log"
filetype:sql inurl:wp-content/backup-*
intext:"Welcome to phpMyAdmin"
intitle:"Login — WordPress"
intext:"Powered by WordPress"
3. Database-Related Dorks
inurl:/phpmyadmin/index.php
intext:"phpMyAdmin MySQL-Dump" filetype:sql
inurl:/db/websql/
inurl:/phpPgAdmin/index.php
intext:"phpPgAdmin — Login"
4. Dorks for Finding Vulnerabilities
intext:"Error Message" intext:"MySQL server" intext:"on * using password:"
intext:"Warning: mysql_connect()" intext:"on line" filetype:php
5. Additional Examples & Usage
Cache Search:

cache:www.google.com
Shows Google’s cached version of a webpage.
Link Search:

link:www.google.com
Lists pages linking to the specified URL.
Related Search:

related:www.google.com
Finds pages similar to the given website.
Info Search:

info:www.google.com
Displays information Google has about a website.
Definition Search:

define:cybersecurity
Gives the definition of “cybersecurity”.
Site-Specific Search:

site:github.com ishanoshada
Searches for pages mentioning “ishanoshada” on GitHub.
All in Title / URL:

allintitle: google search
allinurl: google search
6. Categories to Explore
🔍 Webcams – Peeking into the World
inurl:/view.shtml
intitle:"Live View / - AXIS"
inurl:/control/userimage.html
intitle:"Toshiba Network Camera" user login
intitle:"i-Catcher Console - Web Monitor"
💉 SQL Injection (SQLi)
inurl:"product.php?pid="
inurl:"category.php?id="
inurl:"news.php?id="
inurl:"gallery.php?id="
inurl:"article.php?id="
inurl:"profile.php?id="
inurl:"product-list.php?id="
inurl:"product-detail.php?id="
🥷 Cross-Site Scripting (XSS)
inurl:"search.php?q="
inurl:"results.php?q="
inurl:"gallery.php?name="
inurl:"blog.php?title="
inurl:"category.php?name="
inurl:"faq.php?question="
inurl:"feedback.php?comment="
🛡️ Vulnerable Servers
intitle:"Test Page for the Apache Web Server on Fedora Core"
intitle:"Index of" "CentOS" "Test Page"
intitle:"Test Page for the Nginx HTTP Server"
🔒 Sensitive Directories
intitle:"Index of /admin"
intitle:"Index of /backup"
intitle:"Index of /config"
💽 Database Files
filetype:sql intext:username password
filetype:sql "insert into" (pass|passwd|password)
🚪 Login Pages
intitle:"Login" inurl:/login
intitle:"Login" inurl:/signin
📡 Network Devices
intitle:"RouterOS" inurl:/winbox
intitle:"Ubiquiti" intext:"airOS"
🎥 CCTV Systems
intitle:"DVR Login" inurl:/login.htm
🔐 Apache Tomcat
intitle:"Apache Tomcat" intext:"Apache Tomcat"
🛑 Error Messages
intext:"Error 404: Not Found"
🗃️ Git Repository Files
filetype:gitweb inurl:git
⚙️ Configuration Files
filetype:conf inurl:web.config
💡 PHP Info Files
filetype:php inurl:info
📜 Wordpress Sites
inurl:/wp-admin
📁 Open Directory Listings
intitle:"Index of /" + "backup"
🌟 Google Drive Links
inurl:"/uc?id="
📜 Wordpress Configuration Files
filetype:txt inurl:wp-config
🔐 AWS Access Keys
filetype:pem intext:PRIVATE KEY
🗃️ Additional Configuration Files
filetype:env intext:AWS_SECRET_ACCESS_KEY
