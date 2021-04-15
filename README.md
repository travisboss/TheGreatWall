<h1>Upated to adblock style syntax</h1>

<h3>I have moved this list off of The Great Wall DoH and moved to https://github.com/oneoffdallas/dohservers</h3>

## What is DNS-over-HTTPS (DoH) ?

DoH is a protocol introduced in 2018 as a solution to improve DNS security by encrypting queries through HTTPS, which is advertised as a method to prevent your ISP from tracking your activity, allow you to bypass censorship and protect you against DNS data manipulation (MiMT). In the start of 2020, popular web-browser like <a href="https://arstechnica.com/information-technology/2020/02/firefox-turns-encrypted-dns-on-by-default-to-thwart-snooping-isps/"> Mozilla has started to turn DoH by default in the US</a> and others are <a href="https://blog.chromium.org/2019/09/experimenting-with-same-provider-dns.html"> experimenting it</a>. Microsoft is also considering <a href="https://www.bleepingcomputer.com/news/microsoft/microsoft-is-adding-dns-over-https-doh-to-windows-10/">the addition of DoH in Windows 10</a>.

### But wait... DoH isn't supposed to be a good thing ?

While bringing encryption is always an important thing, including in oppressive countries, DoH isn't a bulletproof solution and may actually cause more problem than it solve. **The rise of service providing DoH, especially US companies like Google or Cloudflare, could harm your privacy by offering additional tracking capabilities** (ex : TLS resumption, which allow to reuse a previous encrypted state for future connection to the same server, could be used to track your browser across IP adress changes) **and centralizing DNS traffic into popular DoH resolver.**

**But moreover, programs and malwares could abuse public DoH provider to evade DNS filtering (like Pihole) and communicate with telemetry service or command-and-control server. See <a href="https://www.trendmicro.com/vinfo/us/security/news/cybercrime-and-digital-threats/new-godlua-backdoor-found-abusing-dns-over-https-doh-protocol">Godlua malware</a>.**

### :warning: Disclaimer

**Theses lists (updated every month) has been created for security purpose ONLY**. There are not a tool to prevent your employee from bypassing the fact that you're monitoring/blocking their online activity ! If you suspect your entity to do so, consider using a VPN or Tor Browser.

You can also block `port 853` for DNS over TLS (DoT)

## An alternative way : increase DoH visibility

Blocking DoH entirely might not be the best approch for everyone, especially if your company wants the benefits of using encrypted DNS while being able to analyse suspicious communications. **<a href="https://www.sans.org/reading-room/whitepapers/dns/dealing-doh-methods-increase-dns-visibility-doh-gains-traction-39560"> This paper </a> demonstrate the possibility of redirecting all traffic from `port 453` to PolarProxy and Security Onion, allowing you to analyse DoH traffic in an unencrypted form.**

## Additionnal ressources :blue_book:

- <a href="https://www.youtube.com/watch?v=pjin3nv8jAo"> NLNOG 2019 - DNS over HTTPS considerations</a>.

- <a href="https://www.ietf.org/archive/id/draft-doh-reid-operator-00.txt">DoH draft for the IETF</a> ("Privacy Concerns" and "Security Considerations").

<p align="right"> * Wall icon drawed by Eucalyp (flaticon.com)
