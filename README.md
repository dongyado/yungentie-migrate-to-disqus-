# gentie-migrate-to-disqus
 convert netease gentie comments  data file to disqus comment data file 

## disqus comment xml format

see https://help.disqus.com/customer/portal/articles/472150

~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0"
xmlns:content="http://purl.org/rss/1.0/modules/content/"
xmlns:dsq="http://www.disqus.com/"
xmlns:dc="http://purl.org/dc/elements/1.1/"
xmlns:wp="http://wordpress.org/export/1.0/"
>
<channel>
<item>
<!-- title of article -->
<title>Foo bar</title>
<!-- absolute URI to article -->
<link>http://foo.com/example</link>
<!-- body of the page or post; use cdata; html allowed (though will be formatted to DISQUS specs) -->
<content:encoded><![CDATA[Hello world]]></content:encoded>
<!-- value used within disqus_identifier; usually internal identifier of article -->
<dsq:thread_identifier>disqus_identifier</dsq:thread_identifier>
<!-- creation date of thread (article), in GMT. Must be YYYY-MM-DD HH:MM:SS 24-hour format. -->
<wp:post_date_gmt>2010-09-20 09:13:44</wp:post_date_gmt>
<!-- open/closed values are acceptable -->
<wp:comment_status>open</wp:comment_status>
<wp:comment>
<!-- sso only; see docs -->
<dsq:remote>
<!-- unique internal identifier; username, user id, etc. -->
<dsq:id>user id</dsq:id>
<!-- avatar -->
<dsq:avatar>http://url.to/avatar.png</dsq:avatar>
</dsq:remote>
<!-- internal id of comment -->
<wp:comment_id>65</wp:comment_id>
<!-- author display name -->
<wp:comment_author>Foo Bar</wp:comment_author>
<!-- author email address -->
<wp:comment_author_email>foo@bar.com</wp:comment_author_email>
<!-- author url, optional -->
<wp:comment_author_url>http://www.foo.bar/</wp:comment_author_url>
<!-- author ip address -->
<wp:comment_author_IP>93.48.67.119</wp:comment_author_IP>
<!-- comment datetime, in GMT. Must be YYYY-MM-DD HH:MM:SS 24-hour format. -->
<wp:comment_date_gmt>2010-09-20 13:19:10</wp:comment_date_gmt>
<!-- comment body; use cdata; html allowed (though will be formatted to DISQUS specs) -->
<wp:comment_content><![CDATA[Hello world]]></wp:comment_content>
<!-- is this comment approved? 0/1 -->
<wp:comment_approved>1</wp:comment_approved>
<!-- parent id (match up with wp:comment_id) -->
<wp:comment_parent>0</wp:comment_parent>
</wp:comment>
</item>
</channel>
</rss>
~~~
