CakePHP-Date-Format-Helper
==========================

<p>A CakePHP helper to format dates consistently throughout an application</p>

<h2>Description</h2>
<p>This is a simple helper that allows you to consistently format dates throughout your application. If someone suddenly decides that dates should look like 1/1/2013 instead of 01-01-2013, you will just need to change it in one place. It includes options to display either the date part or time part or both. It also includes the option to pass in a time offset for dealing with timezones.</p>

<h2>Requirements</h2>
CakePHP 2.x

<h2>Installation</h2>
<p>Copy the DateFormatHelper.php file to <code>/app/View/Helper directory.</code></p>

<h2>Setup</h2>
<p>If you want the Date Format helper available to all controllers, enable it using the <code>$helpers</code> property in /app/Controller/AppController.php:</p>
<pre><code>public $helpers = array('DateFormat');</code></pre>

<p>You might have other Helpers already enabled in the helpers array. If so, add the DateFormat helper to the array:</p>
<pre><code>public $helpers = array('Html', 'Session', 'Form', 'Text', 'DateFormat');</code></pre>

<h2>Usage</h2>

<h2>License</h2>
<p>Copyright (c) 2013 William Rollins</p>

<p>Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:</p>

<p>The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.</p>

<p>THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.</p>
