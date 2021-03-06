proxysocket
===========
Portable C library for proxy client support, designed to be used as a drop-in replacement for connect().

Description
-----------
Cross-platform C library to establish TCP connections using a proxy.

Supports different connection methods:
 - no proxy (optionally allowing to bind to a local address and/or port)
 - HTTP proxy: only CONNECT method, only without authentication or basic authentication
 - SOCKS4/SOCKS4A: without IDENT functionality
 - SOCKS5 (RFC 1928): only username/password authentication or no authentication

Features:
 - Currently only support IPv4 TCP connections.
 - Returns a standard operating system SOCKET that can be manipulated by standard operating system functions like send() and recv().
 - Option to perform name lookups on the proxy server.
 - Supports daisy-chaining multiple proxies.
 - Can also be used for direct connections (without proxy) optionally binding to a local address and/or port.
 - Includes a demo program that uses ipify.org to detect the public IP address being used.
 - Portable across different platforms (tested on Windows, Linux, macOS).
 
Goals
-----
Portability across platfoms (including Windows, Linux and macOS).

The returned SOCKET is a standard operating system connection handle as returned by socket(), allowing for an easy replacement of socket() and connect().

Support for IPv4 TCP connections only. Also, besides the supported proxy protocols, no specific protocol support (like HTTP or SSL) is included.

Dependancies
------------
None

License
-------
proxysocket is released under the terms of the MIT License (MIT), see LICENSE.txt.

