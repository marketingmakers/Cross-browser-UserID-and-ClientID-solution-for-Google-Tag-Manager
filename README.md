# Cross-browser-UserID-and-ClientID-solution-for-Google-Tag-Manager
<h1>Cross-browser User-ID and Client-ID solution for Google Tag Manager</h1>
<p><strong> Due to this solution you will be able to identify one user through unlimited number of sites you own. Every user will receive unique client-id first time he/she/it visits your site. When you assign the user unique user-id from your database/CRM/eshop, you will be able to identify the same user on all your sites. </strong></p>

<h2>How it works?</h2>
<p>There are two files: <code>parent.html</code> and <code>uniqueid.html</code> (child). Child script is included in the parent as <code>&lt;iframe&gt;</code>. Due to <code>window.postMessage()</code> parent and child can communicate. Child script checks variables, create value of client-id, create and maintain cookies and send dataLayer value to parent. When values are sent, <code>trackid</code> event is fired.</p> 
 <ul>
   <li>First time user comes to any of your sites, cliend-id is assigned. Client ID is created from <code>random number + timestamp + another random number</code>. This ID is sent do dataLayer. You may use it in Google Tag Manager or anywhere else.  <br />
 <img src="https://resources.marketingmakers.net/useriddemo/only_clientid.png" alt="Client ID" style="margin: 5px 0;" /> <br />
  Value is saved in cookie and loaded next time user visits the site.       </li>
   <li>When user visits a site and the site provides user-id, both client-id and user-id is sent to dataLayer. User-id is created as <code>given user id + actual hostname</code><br /> 
  <img src="https://resources.marketingmakers.net/useriddemo/user_id.png" alt="User ID" style="margin: 5px 0;"  /></li>
</ul>
<p>That's all! Easy and working.</p>

<h2>Limitations and possible problems</h2>
<p>This solution has not been tested enough. It contains many conditions for several situations. Such as how should the script react if user-id is not set-up, how to react for the first time user-id is provided, how to react second and more times user visited the site etc. Script has not been tested on a heavy traffic website or on various types of mobile devices and browsers. The most testing was made in Google Chrome on desktop. If you notice any problem, please let us know on <a href="https://github.com/marketingmakers/Cross-browser-UserID-and-ClientID-solution-for-Google-Tag-Manager" rel="nofollow" target="_blank">GitHub</a>.</p>

<h2>Debugging</h2>
<p>You can use any tool that can read JavaScript variables and cookies, e.g. WASP, Chrome console or Google Tag Assistant for dataLayer. </p>

<p>Try demo at <a href="https://resources.marketingmakers.net/useriddemo/parent.html" target="_blank">https://resources.marketingmakers.net/useriddemo/parent.html</a></p>

<h2>Credits and Licence</h2> 
<p>This solution is published with courtesy of <a href="https://www.svetzitrka.cz/" title="Go to website" target="_blank">SvetZitrka.cz</a> to whom the solution was originally created. Thank you for the permission! The solution was created by <a href="https://MarketingMakers.net" title="Go to website" target="_blank">Marketing Makers</a>, Czech performance marketing agency.</p>
<p>Feel free to use, change and replicate the solution. Please, always keep the credits of SvetZitrka.cz and MarketingMakers.net</p>

<p>Updated: 10/15/2016</p>
