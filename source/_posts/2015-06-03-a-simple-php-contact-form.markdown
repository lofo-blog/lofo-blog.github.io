---
layout: post
title: "A Simple PHP Contact Form"
date: 2015-06-03 12:08:07 -0500
comments: true
categories: PHP
keywords: php, contact form
---
When you need user to send feedback to your email, you can use contact form. In this tutorial you'll learn how to create contact form with php script.

####Overview

In this tutorial, create 2 files<br>
1. contact.php <br>
2. send_contact.php <br>

Steps<br>
1. Create file contact.php.<br>
2. Create file send_contact.php.<br>
<!--more-->

####Step1: Create File Contact.php

<img src="/images/contact_form.gif"/>

```
<table width="400" border="0" align="center" cellpadding="3" cellspacing="1">
<tr>
<td><strong>Contact Form </strong></td>
</tr>
</table>
<table width="400" border="0" align="center" cellpadding="0" cellspacing="1">
<tr>
<td><form name="form1" method="post" action="send_contact.php">
<table width="100%" border="0" cellspacing="1" cellpadding="3">
<tr>
<td width="16%">Subject</td>
<td width="2%">:</td>
<td width="82%"><input name="subject" type="text" id="subject" size="50"></td>
</tr>
<tr>
<td>Detail</td>
<td>:</td>
<td><textarea name="detail" cols="50" rows="4" id="detail"></textarea></td>
</tr>
<tr>
<td>Name</td>
<td>:</td>
<td><input name="name" type="text" id="name" size="50"></td>
</tr>
<tr>
<td>Email</td>
<td>:</td>
<td><input name="customer_mail" type="text" id="customer_mail" size="50"></td>
</tr>
<tr>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td><input type="submit" name="Submit" value="Submit"> <input type="reset" name="Submit2" value="Reset"></td>
</tr>
</table>
</form>
</td>
</tr>
</table>
```

####Step1: Create File Send_Contact.php

<img src="/images/contact_form_view.gif"/>

```
<?php

// Contact subject
$subject ="$subject"; 

// Details
$message="$detail";

// Mail of sender
$mail_from="$customer_mail"; 

// From 
$header="from: $name <$mail_from>";

// Enter your email address
$to ='someone@somewhere.com';
$send_contact=mail($to,$subject,$message,$header);

// Check, if message sent to your email 
// display message "We've recived your information"
if($send_contact){
echo "We've recived your contact information";
}
else {
echo "ERROR";
}
?>

```