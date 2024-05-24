---
date: 2024-05-18 15:31:00
layout: post
title: What Happens When You Google Something?
subtitle: 'How webpages load in the browser'
description: >-
  When you visit a webpage it instantly loads, but what is really happening?
image: >-
  https://res.cloudinary.com/doka7zxx9/image/upload/v1716063513/Post1_i99k5v.jpg
optimized_image: >-
  https://res.cloudinary.com/doka7zxx9/image/upload/v1716063513/Post1_i99k5v.jpg
category: Networking
tags:
  - welcome
  - blog
  - Google
  - internet
  - dns
  - IP address
  - search engine
  - HTTP
author: Cameron Cruz
paginate: true
---
Who won the <a href="https://www.espn.com/mlb/worldseries/history/winners">World Series</a> in 2017? Can dogs eat apples? Is Europe a country? These are all very important questions to ask, and in the not so distant past, it might have been a real challenge to answer them. Lucky for us, today we have the knowledge of the entire globe right at our fingertips. We are now always just one “Google it” away from finding the answer. Whether staying informed on current events, reading about health and wellness, or learning about scientific phenomena, Google is a vault of human's collective knowledge. 

> The verb "Google" was added to the Oxford English Dictionary on June 15, 2006.

But what really happens when we Google something? What's actually going on behind the scenes of your computer? Is Google the internet?

### The Internet

First things first, Google is not the internet. The internet is a vast network  (grouping) of computers from all over the world. This network of computers is what connects all of our ideas, data and resources. Without the internet, you wouldn’t be able to stream your favorite Netflix shows, buy your favorite Amazon items, or stay connected with your friends through social media. You wouldn’t even have the opportunity to read this blog post. So much of our daily routine revolves around the internet.

### Surfing the Web

Most of the time, when you think about the internet, you're thinking about using a web browser to visit a website on the internet. Some popular browsers are Google Chrome, Microsoft Edge, Firefox, Safari, etc. Inside of these browsers are search engines, which allow users to search the internet for information using keywords. Search engines work to determine which websites to display in the search results, with the intention of helping users find relevant information to their query. Google Search is a leading search engine that indexes billions of web pages in less than a tenth of a second.

> Google processes about 8.5 billion searches per day, which is equivalent to 99,000 search queries per second.

Google Search uses software known as web crawlers to explore the web to find new websites to add to its index. This index is what allows users to quickly find relevant websites in near real-time to explore nearly any category. This means that Googling a website is simply a web-based search to find information on the internet through keywords or phrases. 


So what happens when you Google a website? Let's say you wanted to visit Amazon to buy a few things. After opening Google Chrome, you type **Amazon.com** in the address bar, and press the enter key. The webpage instantly loads, but what just happened?

### Web Servers

First, it's important to quickly define what a website really is. A website is simply a collection of files that can tell your browser how to display a webpage and its data. These files are housed on a computer called a web server, whose sole purpose is to deliver these files to computers around the world. Once delivered, your computer renders the files in the browser to load the website you requested.

So now we know that **Amazon.com** is simply a collection of files and data that live on a server somewhere in the world. However, in order to connect to the web server, our computer has to know where to send a connection to.

### IP Addresses

Luckily, all computers connected to the internet have a unique address that's used to identify and locate one another. This address is called an IP address or an internet protocol address. It is through IP addresses that computers can locate each other when they need to communicate. This means the web server that holds the files for **Amazon.com** has a unique IP address.

> You can use the command line utility **nslookup** to discover the IP address or DNS record of a specific domain name (website). This image is an example of using the tool to find one of the IP addresses for **Amazon.com**.

![Nslookup](../assets/img/uploads/Nslookup(Post1).png)
*54.239.28.85 (Amazon.com)*

### Domain Name System (DNS)

While computers can find this web server through an IP address, it is much easier for humans to remember the domain (website) name. So how does the computer translate the domain name to the corresponding IP address? It does this by using the Domain Name System or DNS.

The Domain Name System (DNS) is a protocol, or set of rules, that translates a domain name into an IP address. You can think of DNS like the contacts app on your phone. The name of the contact is the domain name, and the phone number is the IP address. DNS allows us to find the IP address of a computer based on the domain name. This process is called a DNS lookup. The DNS process is complex, and I will discuss this further in a future post. For now, just know that the DNS process will eventually find the DNS record with the IP address. So, when we type in **Amazon.com** into the web browser, DNS finds the corresponding IP address for the website and provides it to our computer.

### Establish TCP Connection to the Web Server

Now your computer has the IP address of **Amazon.com**, so it will establish a connection with the web server through that IP address. This connection will be a TCP (Transmission Control Protocol) connection, and if the connection is encrypted with HTTPS, a TLS (Transport Layer Security) handshake will also occur.  A TLS handshake works to set up an encryption between the Amazon web server and your device. This maintains the confidentiality and integrity of the data you are requesting from the web server. In practice, it prevents anyone malicious from spying on your connections through the browser. Again, these protocols are detailed, and will be discussed in a future post.

### Browser Sends HTTP Request to Web Server

Once this connection has been established to the web server, your computer is going to send a HTTP GET request to the server. This is simply your computer asking the web server for the file contents of the Amazon.com website. When you enter a URL into your web browser and press enter, it typically sends an HTTP GET request to the server hosting that website. GET requests retreive data such as web pages, images, videos, etc.


### Web Server Sends Back a Response

The web server then processes this request and sends back a response to your computer. While the web server can return a set of static files to your computer, that is not always the case. Most of the time, the web contents are dynamic and the server has to generate a dynamic resource to send back in the response.

### Browser Loads the Content

After receiving the response from the web server, your browser inspect its contents to render the site in your browser. The response is usually a combination of HTML, CSS, Javascript and additional data. Once this information is loaded by your browser you will be presented with the landing page for Amazon.com.

### Recap

Here is an overview of the steps taken when you type a URL into a web browser.

1. User types a URL into the browser's address bar
2. A DNS lookup finds the IP address associated with the domain name
3. The browser estabishes a TCP connection with the web server
4. The browser sends a HTTP (GET) request to the web server
5. The server recieves the request, and sends back a response
6. The browser recieves the response and renders the content

Everything we just talked about (and much more) occurs in a second or two. It’s easy to forget, but the internet is simply the movement of data in the form of light or electrical pulses. This data, also called ‘bits’, is moving at ⅔ the speed of light. It is incredible how fast the internet really is.

You now know that Google is not the internet. It is a search engine that has indexed over 130 trillion web pages. When you visit these webpages, many steps occur behind the scenes. Hopefully you now know a bit more about that process and can move onto the more important questions of life. Such as, how to play the guitar? Are there aliens in Area 51? What's the meaning of life? If you don't know...just Google it.
<br/><br/>