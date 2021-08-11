# Change your browser !

## Informations

Challenge from [W3C_challs/web](https://w3challs.com/challenges/list/web).

Attachements:
 - Challenge link: http://change-browser.hax.w3challs.com/

## Analysis

By reaching the challenge, the explanation of the flag location and how to get it is directly given.
We should use a browser with a specific name to make the server returning a pae than contain the flag.

##  Solution

The browser name is given to the server inside request headers. To change it, we should change a header variable named 'User_Agent'.
Send a get request (by any ways) with 'User-Agent'='W3Challs_browser' to http://change-browser.hax.w3challs.com/ will give us as a response, an html code with the flag inside.

```html
<!DOCTYPE HTML>
<html>

<head>
	<title>Change your browser</title>
	<meta name="owner" content="W3Challs" />
	<meta name="publisher" content="w3challs" />
	<meta name="copyright" content="w3challs" />
	<meta name="robots" content="noindex,nofollow">
	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
</head>

<body>

	<p align="center">Congratz! The flag to solve this challenge is
		"W3C{now_that_we_have_the_right_browser_lets_get_the_party_started}"</p>

</body>

</html>
```
