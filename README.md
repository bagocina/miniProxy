# miniProxy

*by Joshua Dick*

*[http://joshdick.github.io/miniProxy][1]*

*edited by Jan Neurocny*

*[https://github.com/bagocina/miniProxy][5]*

---

## About miniProxy

miniProxy is a simple web proxy written in PHP that can allow you to bypass Internet content filters, or to browse the internet anonymously. miniProxy is licensed under the [GNU GPL v3][2]. miniProxy is the successor to [pageForward][3].

## Prerequisites

miniProxy should be able to run on any web server with PHP 5.4.7 or later. miniProxy requires PHP's `curl` and `mbstring` extensions to be installed.

## Installation and Use

Simply copy `miniProxy.php` to your web server (it's okay to rename it) and access it directly. That's it! You'll be presented with further usage instructions.

miniProxy doesn't require any configuration out of the box, but configuration options are available; see the top of `miniProxy.php` for details.

## Known Limitations

miniProxy has several known limitations. Some of them may be fixed in future releases. For now, they include:

* `<object>` tags are not handled
* No cookie support
* Basic AJAX support, but only for browsers that use `XMLHttpRequest`

## Code changes by Jan Neurocny
* Adding variable $useCustomProxy, to turn on using custom defined proxy server via GET params (miniProxy.php?ip=xxx.xxx.xxx.xxx&port=8080&url=http://example.net). ([commit 42ca2a2][6])
* Adding variable $useCustomUseragent, to turn on using custom defined UserAgent. ([commit 42ca2a2][6])
* Adding parameter "protocol", to set CURLOPT_PROXYTYPE. 
  * http - CURLPROXY_HTTP
  * socks4 - CURLPROXY_SOCKS4
  * socks5 - CURLPROXY_SOCKS5
  * socks4a - CURLPROXY_SOCKS4A
  * socks5_host - CURLPROXY_SOCKS5_HOSTNAME

## Contact and Feedback

If you'd like to contribute to miniProxy or file a bug or feature request, please visit [its GitHub page][4].

  [1]: http://joshdick.github.io/miniProxy
  [2]: http://www.gnu.org/licenses/gpl.html
  [3]: http://pageforward.sf.net
  [4]: https://github.com/joshdick/miniProxy
  [5]: https://github.com/bagocina/miniProxy
  [6]: https://github.com/bagocina/miniProxy/commit/42ca2a29e53fa2f2f97fef78700977ec057bcf82