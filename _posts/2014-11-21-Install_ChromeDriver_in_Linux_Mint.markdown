---
layout: post
title:  "Install ChromeDriver in Linux Mint"
date:   2014-11-21 11:41:51
categories: jekyll update
---

1. Install unzip

   sudo apt-get install unzip

2. Download last version of ChromeDriver and unzip it

   wget -N http://chromedriver.storage.googleapis.com/2.9/chromedriver_linux64.zip -P ~/Downloads

   unzip ~/Downloads/chromedriver_linux64.zip -d ~/Downloads

3. Make it executable and move to /usr/local/share

   chmod +x ~/Downloads/chromedriver

   sudo mv -f ~/Downloads/chromedriver /usr/local/share/chromedriver

4. Create symbolic links

   sudo ln -s /usr/local/share/chromedriver /usr/local/bin/chromedriver

   sudo ln -s /usr/local/share/chromedriver /usr/bin/chromedriver


