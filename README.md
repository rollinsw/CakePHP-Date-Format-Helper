CakePHP-Date-Format-Helper
==========================

A CakePHP helper to format dates consistently throughout an application

<h1>Requirements</h1>
CakePHP 2.x

<h1>Install and Setup</h1>

If you want the Date Format helper available to all controllers, enable it using the <code>$helpers</code> property in /app/Controller/AppController.php:
<pre><code>public $helpers = array('DateFormat');</code></pre>

You might have other Helpers already enabled in the helpers array. If so, add the DateFormat helper to the array:
<pre><code>public $helpers = array('Html', 'Session', 'Form', 'Text', 'DateFormat');</code></pre>
