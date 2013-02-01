CakePHP-Date-Format-Helper
==========================

<p>A CakePHP helper to format dates consistently throughout an application</p>

<h2>Description</h2>
<p>This is a simple helper that allows you to consistently format dates throughout your application. If someone suddenly decides that dates should look like 1/1/2013 instead of 01-01-2013, you will just need to change it in one place. It includes options to display either the date part or time part or both. It also includes the option to pass in a time offset for dealing with timezones.</p>

<p>I created this when working on a project where the client changed their mind several times about how dates should be formatted on the site. This allowed me to easily make this change in one place.</p>

<h2>Requirements</h2>
CakePHP 2.x

<h2>Installation</h2>
<p>Copy the <code>DateFormatHelper.php</code> file to <code>/app/View/Helper</code></p>

<h2>Setup</h2>
<p>Edit the following variable in <code>DateFormatHelper.php</code> to adjust the helper defaults:
<ul>
<li><strong>dateOnlyFormat:</strong> PHP date format options to use when only date is displayed</li>
<li><strong>timeOnlyFormat:</strong> PHP date format options to use when only time is displayed</li>
<li><strong>dateTimeFormat:</strong> PHP date format options to use when both date and time are displayed</li>
<li><strong>defaultDatePartDisplay:</strong> True/False default setting for date part display</li>
<li><strong>defaultTimePartDisplay:</strong> True/False default setting for time part display</li>
<li><strong>defaultOffset:</strong> Default value for time offset in hours</li>
</ul>
</p>

<p>If you want the Date Format helper available to all controllers, enable it using the <code>$helpers</code> property in /app/Controller/AppController.php:</p>
<pre><code>public $helpers = array('DateFormat');</code></pre>

<p>You might have other Helpers already enabled in the helpers array. If so, add the DateFormat helper to the array:</p>
<pre><code>public $helpers = array('Html', 'Session', 'Form', 'Text', 'DateFormat');</code></pre>

<h2>Usage</h2>
<p>Use the following to format a date when displaying in a view: <code>echo $this->DateFormat->formatDate($dateString, $options);</code> where $dateString is your date as a string and $options is an array that contains these options:
<ul>
<li><strong>displayDatePart:</strong> True/False display the date portion</li>
<li><strong>displayTimePart:</strong> True/False display the time portion</li>
<li><strong>offset:</strong> An offset for the date in hours. Intended to be used to adjust date/time based on timezones.</li>
</ul>
</p>

<pre><code>
$myDate = '2013-01-21 15:56:41';

// Would echo something like: 1/21/2013
echo $this->DateFormat->formatDate($myDate, array(
	'displayDatePart'=>true, 
	'displayTimePart'=>false, 
	'offset'=>-5)
);

// Would echo something like: 1/21/2013 10:56
echo $this->DateFormat->formatDate($myDate, array(
	'displayDatePart'=>true, 
	'displayTimePart'=>true, 
	'offset'=>-5)
);
</code></pre>

<h2>License</h2>
<p>Copyright (c) 2013 William Rollins</p>

<p>Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:</p>

<p>The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.</p>

<p>THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.</p>
