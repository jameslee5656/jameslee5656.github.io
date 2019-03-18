---
layout: "post"
title:  "1.Introduction to Tracker"
date:   2019-3-16
categories: Tracker
---
<header>
	<p>This is a introduction to our on going project.</p>
</header>

<div class="row">	
	<div style="padding-right: 1.2em">
		<iframe width="588" height="330" src="/vedio/clipForIntro.mp4" frameborder="0" allowfullscreen></iframe>
	</div> To start all, here is a vedio to give you a better perspective of our project. I will introduce this project through different roles and functionalities includes Web, data tranmit station, cell phone, sport bands, server.
</div>
<h2 style="padding-top: 1.2em;">Functionalities</h2>
<div class="row">
	<div class="12u 12u$(small)">
		<dl>
			<dt><h3>Web</h3></dt>
			<dd>
				<ul>
					<li>
						We use map to display the outdoor user, our system will according to the GPS data to auto user are walking or riding a bike.
					</li>
					<li>
						It display both realtime and history health data (heart rate, blood oxygen rate, step counts)
					</li>
					<li>
						According to different group and user, we map out GPS hot zone analysis. 
					</li>
					<li>
						When users`s heart rate is too high, it will send out the warning signals.
					</li>
				</ul>
			</dd>
			<dt><h3>Data transmit relation station</h3></dt>
			<dd>
				<ul>
					<div class='row'>
						<img src="/images/PI.jpg" style="width: 32em;height:26em;">
					</div>
					<li>
						Connect with Miband and transmit health data through NBIOT
					</li>
				</ul>
			</dd>
			<dt><h3>Cell phone</h3></dt>
			<dd>
				<ul>
					<li>
						Receive data, transmit warning signal.
					</li>
				</ul>
			</dd>
			<dt><h3>Sport Band</h3></dt>
			<dd>
				<ul>
					<li>
						We use two types of sport band
						<div class='row' style="padding-bottom: 1.2em;">
							<div class="column">
								<img src="/images/miband.jpeg" style="width: 14em;height:20em; padding: 1.4em;">
								<h4>MiBand 2</h4>
							</div>
							<div class="column">
								<img src="/images/golife.png" style="width: 20em;height:20em;">
								<h4>Golife Care-X-HR</h4>
							</div>
						</div>
					</li>
				</ul>
			</dd>
			<dt><h3>Server</h3></dt>
			<dd>
				<ul>
					<li>
						System : Ubuntu 16.04
					</li>
					<li>
						Data Base : Mongo DB, For data Storing, Retrieving ,and Delete
					</li>
				</ul>
			</dd>
		</dl>
	</div>		
</div>