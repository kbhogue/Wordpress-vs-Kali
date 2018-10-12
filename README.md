# Wordpress-vs-Kali
# Week 7 Pentesting Assignment
> Find 3-5 vulnerabilities in an older version of Wordpress.

Time Spent: 10 hours


1\. XSS in Embedded Youtube Videos
* Vulnerabilities: XSS
* Tested in Wordpress 4.2 and fixed in Wordpress 4.2.13
* Steps to Recreate: Retrieve iframe embedded video link from Youtube. Add new post in Wordpress with the embedded video as the content. Add your XSS to the end of the main embedded video statement. I used onload=alert(123). The final post was <iframe width="560" height="315" src="https://www.youtube.com/embed/9SGHPQ2FVm8" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen onload=alert(123)></iframe>. Alert will pop up every time the video loads.
![](https://github.com/kbhogue/Wordpress-vs-Kali/blob/master/gif1.gif)

2\. XSS in Page Comment
* Vulnerabilities: XSS
* Tested in 4.2 and fixed in 4.2
* Steps to Recreate: Go to the comments section of a published Wordpress page. Insert a XSS command. I used "<script>onload=alert(document.cookie);</script>" to make endless alerts pop up outputting the document cookies. 
![](https://github.com/kbhogue/Wordpress-vs-Kali/blob/master/gif2.gif)

3\. XSS at the End of an URL
* Vulnerabilities: XSS
* Tested in 4.2 and fixed in 4.2.5
* Steps to Recreate: Create a new post and paste in a website URL. At the end, add your XSS command, with svg at the beginning. I used the following command: "<onload=alert(123)>". An alert will pop up every time the post loads. 
![](https://github.com/kbhogue/Wordpress-vs-Kali/blob/master/gif3.gif)
