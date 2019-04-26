---
title: "Public DNS Server Tool"
excerpt: "Public DNS Server Tool is a small utility for changing the DNS servers in Windows XP, Vista, 7, 8, 8.1 and 10 on the fly."
image:
  path: &image /assets/images/google_public_dns.jpg
  feature: *image
  thumbnail: /assets/images/google_public_dns.jpg
  teaser: /assets/images/google_public_dns.jpg
  caption: "[Photo by **Google DNS Free**](https://developers.google.com/speed/public-dns/)"
tags: [DNS, Free, Tools]
comments: true
comments_locked: true
last_modified_at: 2018-03-11T13:57:09-04:00
---

Public DNS Server Tool is a small utility for changing the DNS servers in Windows XP, Vista, 7, 8, 8.1 and 10 on the fly.

{% figure caption:"Public DNS Server Tool" %}
![Public DNS Server Tool](/assets/images/public-dns-tool-0.jpg)
{% endfigure %}

n the past few years, many public DNS servers have been made available for everyone’s use. Some of them are Cloudflare DNS, OpenDNS, Google, Norton, Comodo Secure etc. These DNS servers offer many security and protection layers in addition to being very fast. Even though these public DNS servers are available for everyone’s use, setting up DNS servers in Windows is not an easy task. Therefore, I have created this little tool Public DNS Server Tool, using which you can easily set the domain name servers in Windows.

{% include boilerplate/adsense-baiviet.md %}


It has been tested to work in Windows XP Professional SP3 (32-bit), Windows Vista SP2 (32-bit), Windows 7 (32-bit), Windows 8 (64-bit) and Windows 10 (32-bit).

You can use a Public DNS Server Tool to quickly switch to a preset pair of public DNS servers. Currently, it has sixteen preset pairs of DNS servers —

- Google Public DNS
- Cloudflare DNS
- Verisign DNS
- OpenDNS
- OpenDNS FamilyShield (blocks sites inappropriate for family)
- Yandex Basic DNS
- Yandex Safe DNS
- Yandex Family DNS
- Norton ConnectSafe A (blocks malicious sites)
- Norton ConnectSafe B (blocks malicious sites + pornography sites)
- Norton ConnectSafe C (blocks malicious sites + pornography sites + non-family sites)
- Comodo Secure DNS (blocks malicious sites)
- Neustar General
- Neustar Threat Protection
- Neustar Family Secure
- Neustar Business Secure
- Backup and Restore

Public DNS Server Tool allows you to backup your DNS server settings. To backup, select Backup → Backup from the menubar. It would ask you a location where you want to save the backup file. The backup file is automatically named with current date and time in the DD-MM-YYYY HH-MM-TT format. The backup file is in the standard Registry script (.REG) format, so you can just double-click on it to restore the DNS server settings inside it. However, it also allows you restore DNS setting from within the Public DNS Server Tool. To restore, select Backup → Restore from the menubar. It would ask you to select a backup REG file. The entries inside the reg file would be automatically inserted into the Windows Registry and DNS servers would be updated.

**Setting up public DNS servers**


[**Download Public DNS Server Tool**](https://www.trishtech.com/downloads/public_dns.zip) to your computer.

Unzip it to any folder you want on your hard disk.

Run Public DNS Server Tool by double-clicking on PublicDNS.exe. Since this tool makes changes to your DNS server settings, it requires administrator privileges. If you are running Windows XP, then you should be logged in as an administrator. If you are running Windows Vista, Windows 7, Windows 8 or Windows 10, then you will be shown UAC (User Account Control) and would be asked to provide administrator login.

First of all backup your current DNS servers by selecting Backup → Backup from the menubar. This is very useful if you later want to restore your original DNS servers.

Choose your Network Interface Card (NIC) from the dropdown list box. If you have only one NIC, then it will be pre-selected. As you select a NIC card, the current DNS server configured for the selected NIC would be shown in big blue text. You can select the checkbox labeled Select all to select all the NIC cards in your system.

Choose a set of public DNS servers from the list. As you select a DNS server, their description would be visible below the list. From the description, you can learn about what benefits a DNS server provides. The website of the selected DNS server is also given.

Finally, click on the Change button at the bottom of the window. It would take a few seconds to change the DNS servers. If even after changing the DNS servers, you see your browser using previous DNS servers, then either press Ctrl + F5 to reload the webpage or restart your web browser.

Please note that DNS server settings are changed only for the selected network interface card. If you have more than one network interface cards, then you should choose the one you use to connect to the internet. You can also choose all the NIC cards, by selecting the checkbox labeled Select all. This way you can change the DNS servers for all the NIC cards in a single click.

If even after changing the DNS servers, you see your browser using previous DNS servers, then close and restart your browser again. If even after restarting the browser, changed DNS servers are not being used, then you may have to restart the Windows.

Adding More Servers to servers.ini
Starting from the version 2.1, Public DNS Server Tool stores all the server data in the servers.ini file. If this file does not exist in the same folder as the PublicDNS.exe, then it creates a default servers.ini file loaded with eight well-known publicly available DNS servers. But if you want to add more DNS servers, then you can simply edit this file and add more servers.

For example, suppose you want to add DNS servers from your own ISP (say RoadRunner) and their primary DNS server is 24.25.227.55, and secondary DNS server is 24.25.227.53. Then just open the servers.ini file in Notepad and add the following at the end of the file :

{% notice info %}

[RoadRunner]
address=24.25.227.55, 24.25.227.53

{% endnotice %}


There should be no space between ‘address’ and ‘=’, or it will fail to load. You will have to close Public DNS Server Tool and restart it so that it can load newly added servers from the servers.ini file.
