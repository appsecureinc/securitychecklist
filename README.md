<h3 style='box-sizing:border-box;margin-bottom:16px;font-size:1.25em;line-height:1.25;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";margin-top:0px;'>Security Checklist for Web Developers by AppSecure <a data-saferedirecturl="https://www.google.com/url?q=https://appsecure.security/&source=gmail&ust=1579166469648000&usg=AFQjCNEn-e3pmuQunDa1J7unngkf-gnrRA" href="https://appsecure.security/" rel="nofollow" style="box-sizing:border-box;background-color:initial;color:rgb(3,102,214);text-decoration-line:none;" target="_blank">https://appsecure.<wbr>security</a></h3>

<h5 style='box-sizing:border-box;margin-top:24px;margin-bottom:16px;font-size:0.875em;line-height:1.25;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";'>
	<a href="https://github.com/AppSecureIndia/security-checklist-for-devs#securing-authentication" style="box-sizing:border-box;background-color:initial;color:rgb(3,102,214);text-decoration-line:none;float:left;padding-right:4px;line-height:1;" target="_blank" data-saferedirecturl="https://www.google.com/url?q=https://github.com/AppSecureIndia/security-checklist-for-devs%23securing-authentication&source=gmail&ust=1579166469648000&usg=AFQjCNEBUrC1PONvXo2our1qyl74C8RiiA"></a>Securing authentication</h5>

<ul style='box-sizing:border-box;padding-left:2em;margin-top:0px;margin-bottom:16px;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";font-size:16px;'>
	<li style="box-sizing:border-box;list-style-type:none;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use HTTPS everywhere - protect all endpoints over SSL encryption</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Sanitize user input - properly sanitize all user input to make sure it does not contain characters which can circumvent application logic</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Store passwords using encryption - store passwords in the database using encryption like bcrypt to restrict retrieval of password in case of breach</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use protective password standards - force user to register using a strong password</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;"> Enforce rate-limiting - rate-limit all authentication requests to prevent brute-force attacks. This can be very dangerous. Anand Prakash, AppSecure discovered a bug on Facebook which allowed anyone to takeover Facebook account by bruteforcing OTPs. Reference :<a data-saferedirecturl="https://www.google.com/url?q=https://www.theverge.com/2016/3/8/11179926/facebook-account-security-flaw-bug-bounty-payout&source=gmail&ust=1579166469648000&usg=AFQjCNGHLS1s5_Ndkq3J063obvwFylmznA" href="https://www.theverge.com/2016/3/8/11179926/facebook-account-security-flaw-bug-bounty-payout" rel="nofollow" style="box-sizing:border-box;background-color:initial;color:rgb(3,102,214);text-decoration-line:none;" target="_blank">https://www.theverge.com/<wbr>2016/3/8/11179926/facebook-<wbr>account-security-flaw-bug-<wbr>bounty-payout</a></li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Suppress verbose error messages - don&rsquo;t print messages confirming the existence of user account, to prevent user enumeration</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Provide unique, unpredictable usernames - if self-registration is disabled, don&rsquo;t use easily guessable usernames, to prevent user enumeration</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Unique password reset tokens - send completely encrypted/random password reset tokens which cannot be guessed by attacker</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Expire password reset tokens - make sure the password reset token expires after a reasonable amount of time</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Implement OAuth properly - prevent open redirects and use the state parameter in OAuth endpoints</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure the HTTP responses for authentication-related requests - don&rsquo;t leak the OTP / password / reset token in response to user&rsquo;s requests</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure JWT tokens - ensure secure use of JWT tokens by validating the algorithm and the signature on the backend</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure &lsquo;Forgot Password&rsquo; - don&rsquo;t rely on user input like host header to generate reset tokens</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure OTP handling and generation - generate minimum 6 digits OTP and make sure it is one-time use only</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Protect against referer leakage - ensure that sensitive tokens like password reset tokens don&rsquo;t get leaked via the referer header to third-party websites</li>
</ul>

<h5 style='box-sizing:border-box;margin-top:24px;margin-bottom:16px;font-size:0.875em;line-height:1.25;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";'>
	<a href="https://github.com/AppSecureIndia/security-checklist-for-devs#securing-session-management" style="box-sizing:border-box;background-color:initial;color:rgb(3,102,214);text-decoration-line:none;float:left;padding-right:4px;line-height:1;" target="_blank" data-saferedirecturl="https://www.google.com/url?q=https://github.com/AppSecureIndia/security-checklist-for-devs%23securing-session-management&source=gmail&ust=1579166469648000&usg=AFQjCNH2h9ig_GfO-IeHP7fxhuVhOmvMOg"></a>Securing session management</h5>

<ul style='box-sizing:border-box;padding-left:2em;margin-top:0px;margin-bottom:16px;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";font-size:16px;'>
	<li style="box-sizing:border-box;list-style-type:none;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure token generation - ensure that all session tokens are reasonably random, are not meaningful, and cannot be brute-forced</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Proper cookie scope - tie the session tokens to only the subdomains which require them, using the domain and path flags</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use HttpOnly, secure and SameSite cookies - use these flags to ensure protection in case of client-side attacks like XSS and CSRF</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure session termination - after user logout or password reset, kill all existing sessions of the user and invalidate all session tokens</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Restrict disclosure of tokens in URLs - don&rsquo;t disclose session tokens in URLs as they might be logged or sent as referer to third party websites</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Prevent token reuse - ensure no session tokens are same for consecutive / concurrent logins</li>
</ul>

<h5 style='box-sizing:border-box;margin-top:24px;margin-bottom:16px;font-size:0.875em;line-height:1.25;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";'>
	<a href="https://github.com/AppSecureIndia/security-checklist-for-devs#securing-access-controls--authorization" style="box-sizing:border-box;background-color:initial;color:rgb(3,102,214);text-decoration-line:none;float:left;padding-right:4px;line-height:1;" target="_blank" data-saferedirecturl="https://www.google.com/url?q=https://github.com/AppSecureIndia/security-checklist-for-devs%23securing-access-controls--authorization&source=gmail&ust=1579166469648000&usg=AFQjCNHxxr-1JqROUjiLLxOkpkSTT01KPw"></a>Securing access controls / authorization</h5>

<ul style='box-sizing:border-box;padding-left:2em;margin-top:0px;margin-bottom:16px;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";font-size:16px;'>
	<li style="box-sizing:border-box;list-style-type:none;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure user identifiers - use RFC compliant UUIDs for every user account</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use JWT - prefer JWT over traditional session tokens for ease of securing</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure static files - developers often forget securing access controls for static files like JPEG etc.</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;"> Secure multi-stage functions - properly enforce access controls over functions which require more than one level of user interaction, eg. directly accessing <a data-saferedirecturl="https://www.google.com/url?q=http://example.com/?step%3D3&source=gmail&ust=1579166469648000&usg=AFQjCNFvi4a6bJZdBnLLGTUepkcgJMAhhA" href="http://example.com/?step=3" target="_blank">example.com/?step=3</a> without going through /?step=2 or /?step=1</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure function names - don&rsquo;t use identifier based functions eg. if an endpoint exists /?action=getUser, then attacker might be able to guess and endpoint like /?action=deleteUser</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure access control methods - don&rsquo;t rely on identifiers like URL parameter, referer headers, HTTP headers to check access level of user; check everything on backend also as client-side checks can be bypassed by user submitted input</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Secure multi-layered access controls - enforce proper access controls for accounts with different levels of privileges to prevent vertical privilege escalation</li>
</ul>

<h4 style='box-sizing:border-box;margin-top:24px;margin-bottom:16px;font-size:16px;line-height:1.25;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";'>
	<a href="https://github.com/AppSecureIndia/security-checklist-for-devs#secure-http-headers" style="box-sizing:border-box;background-color:initial;color:rgb(3,102,214);text-decoration-line:none;float:left;padding-right:4px;line-height:1;" target="_blank" data-saferedirecturl="https://www.google.com/url?q=https://github.com/AppSecureIndia/security-checklist-for-devs%23secure-http-headers&source=gmail&ust=1579166469648000&usg=AFQjCNF1iWt7mCSVOhNwdbQkB39syLykwg"></a>Secure HTTP headers</h4>

<ul style='box-sizing:border-box;padding-left:2em;margin-top:0px;margin-bottom:16px;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";font-size:16px;'>
	<li style="box-sizing:border-box;list-style-type:none;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Add CSP header - use this header in HTTP responses to prevent XSS and client-side injection attacks</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Add CSRF header - use CSRF tokens in HTTP headers to prevent cross site request forgery</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Add X-XSS-Protection header - use this with value set to 1; mode=block to mitigate XSS attacks</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Add HSTS header - tells the browser to load website using only HTTP</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Add X-Frame-Options - use this with value as sameorigin to prevent clickjacking attacks.</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use X-Content-Type-Options: nosniff - to prevent MIME sniffing by browser like IE, which can lead to XSS</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use correct Content-Type headers - the browser should not get confused between JSON, XML and HTML responses, as this inconsistency can also lead to injection attacks like XSS</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use correct caching directives - to prevent caching of sensitive information</li>
</ul>

<h4 style='box-sizing:border-box;margin-top:24px;margin-bottom:16px;font-size:16px;line-height:1.25;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";'>
	<a href="https://github.com/AppSecureIndia/security-checklist-for-devs#miscellaneous---best-practices-to-follow-when-building-applications" style="box-sizing:border-box;background-color:initial;color:rgb(3,102,214);text-decoration-line:none;float:left;padding-right:4px;line-height:1;" target="_blank" data-saferedirecturl="https://www.google.com/url?q=https://github.com/AppSecureIndia/security-checklist-for-devs%23miscellaneous---best-practices-to-follow-when-building-applications&source=gmail&ust=1579166469649000&usg=AFQjCNEotq_cW7xS9UnO799XVgo5cGuWjg"></a>Miscellaneous - best practices to follow when building applications</h4>

<ul style='box-sizing:border-box;padding-left:2em;margin-top:0px;margin-bottom:16px;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";font-size:16px;'>
	<li style="box-sizing:border-box;list-style-type:none;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Validate, encode and sanitize all input in the backend, to prevent against injection attacks like XSS, SQL injection, template injection etc.</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use parameterized queries and prepared statements for building SQL queries in the backend</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;While input validation can be either whitelisted or blacklisted, it is preferable to whitelist data. Whitelisting only passes expected data. In contrast, blacklisting relies on programmers predicting all unexpected data</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Disable directory listing</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Properly configure CORS (wherever applicable) by using proper CORS headers i.e. Access-Control-Allow-Origin, Access-Control-Allow-Methods etc.</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Ensure proper egress filtering to minimize the damage of attacks like SSRF and data exfiltration using out-of-band channels</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Make sure all stacks and modules used in development are updated</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Don&#39;t print stack trace for error messages as they might contain sensitive server information</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use proxies like CloudFlare to protect your website against most attacks, and also to hide the true origin IP of web server</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use proper caching directives to prevent caching of sensitive user info, and also to prevent against attacks like HTTP request smuggling</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Don&rsquo;t leak server info like server version, PHP version etc. in HTTP response as attacker might use this to get publicly available exploits for vulnerable versions</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Use DMARC and SPF records in DNS servers - to protect against email spoofing attacks</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Ensure all unnecessary ports are closed and are not exposed to the internet</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Make use of live monitoring and alerting provisions to detect targeted attacks and bad actors in real-time as quickly as possible</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Don&rsquo;t leave the staging environments exposed to the internet, and don&#39;t use live data for them</li>
	<li style="box-sizing:border-box;list-style-type:none;margin-top:3px;">
		<input type="checkbox" disabled="" style="font:inherit;margin-right:0.2em;margin-bottom:0.25em;overflow:visible;padding:0px;vertical-align:middle;">&nbsp;Check all subdomains for expiry, else they might be vulnerable to subdomain takeovers</li>
</ul>

<p style='box-sizing:border-box;margin-top:0px;color:rgb(36,41,46);font-family:-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";font-size:16px;margin-bottom:0px;'>Visit our blog for our work on Uber, Twitter, Facebook&#39;s bug bounty: <a data-saferedirecturl="https://www.google.com/url?q=https://appsecure.security/blog&source=gmail&ust=1579166469649000&usg=AFQjCNF6pxeh9f8MO63-3FHk2rkBj6IbvQ" href="https://appsecure.security/blog" rel="nofollow" style="box-sizing:border-box;background-color:initial;color:rgb(3,102,214);text-decoration-line:none;" target="_blank">https://appsecure.<wbr>security/blog</a></p>
