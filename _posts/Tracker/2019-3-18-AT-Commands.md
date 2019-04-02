---
layout: "post"
title:  "3.AT Commands"
date:   2019-3-18
categories: Tracker
description: A much comprehended understanding of AT command
---
<h2>What is AT Commands</h2>
<div class='row'>
 	<img src="/images/dongle.jpg" style="width: 26em;height:16em; margin-right: 1.2em;">
 	AT commands are instructions used to control a modem. Each commands start with 'AT' or 'at'. Mostly used in GSM/GPRS modems and mobile phone. Which is the reason our NBIOT Dongle modems are controlled for. The left picture is the device that we are using. It is lierda NB-IoT USB Dongle. The SIM card we're using is provide by Fetnet.
</div><br>
<h2>Testing Software</h2>
This <a href="/releases/download/v1.0.0/sscom5.11a.zip" download>link</a> provide you a testing software which is a Graphical Software to test your modem. (It is exe file so you have to use windows to execute it)
<br>
<h2>Commands that we use</h2>
<ul>
	<li>
		<code>AT</code>use this to test that your modem is all right
		<br>
		return:<code>OK</code>
	</li>
	<li>
		<code>AT+CFUN?</code>, this command ask your modem's radio frequency status
		<ul>
			<b>Returning:</b>
			<li>radio frequency status is open<br>
				<pre style="padding-right: 48em;"><code>+CFUN:1<br>OK</code></pre>
			</li>
			<li>radio frequency status is closed, broken, or SIM card is not correctly connected<br>
				<code>+CFUN:0</code><br>
			</li>
		</ul>
	<li>
		<code>AT+CIMI</code>, this will return your card's IMSI
	</li>
	<li>
		<code>AT+CSQ</code>, return something like +CSQ:16,99 16 means quality of signal(0-31), if this is 99 means you didn't capture signal. Maybe wait for a few seconds if it still is +CSQ:99,99. then maybe you should check your card.
	</li>
	<li><code>AT+CEREG?</code>
		<ul>
			<b>Returning:</b>
			<li>Internet Unregisted, Initial State, Maybe wait a few second<br>
				<code>+CEREG:0,0</code>
			</li>
			<li>Registed Success<br>
				<code>+CEREG:0,1</code>
			</li>
			<li>The route isn't quite good<br>
				<code>+CEREG:0,2</code>
			</li>
		</ul>
	</li>
	<li><code>AT+CGPADDR</code>Return:<code>CGPADDR:0,10.162.113.26</code>This is`nt the external IP but the a wan IP</li>
	<li><code>AT+NPING=XXXX</code>Make sure do this before you try to send a message</li>
	<li><code>AT+NSOCR=DGRAM,17,8888,1</code>Open a UDP port 8888, this is the port that you open locally. Return<pre><code>0
OK</code></pre>The first number is the socket id you may want to store it.
	</li>
	<li><code>AT+NSOST=0,xxxx,60001,2,AB30</code>send a 2 bytes message to the server, the first number is socket number.</li>
	<li>Receive Message, This part didn't have code. If server return something than there will be something like <code>+NSONMI:0,3</code></li>
	<li>The last part, we have to take the message from Dongle <code>AT+NSORF=0,3</code></li>
<!-- </ul> -->