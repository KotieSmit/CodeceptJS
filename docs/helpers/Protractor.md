# amOnPage

[lib/helper/Protractor.js:84-89](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L84-L89 "Source code on GitHub")

Opens a web page in a browser. Requires relative or absolute url.
If url starts with `/`, opens a web page of a site defined in `url` config parameter.

```js
I.amOnPage('/'); // opens main page of website
I.amOnPage('https://github.com'); // opens github
I.amOnPage('/login'); // opens a login page
```

**Parameters**

-   `url`  

# amOutsideAngularApp

[lib/helper/Protractor.js:73-75](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L73-L75 "Source code on GitHub")

Switch to non-Angular mode, 
start using WebDriver instead of Protractor in this session

# appendField

[lib/helper/Protractor.js:195-202](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L195-L202 "Source code on GitHub")

Appends text to a input field or textarea.
Field is located by name, label, CSS or XPath

```js
I.appendField('#myTextField', 'appended');
```

**Parameters**

-   `field`  
-   `value`  

# attachFile

[lib/helper/Protractor.js:161-176](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L161-L176 "Source code on GitHub")

Attaches a file to element located by label, name, CSS or XPath
Path to file is relative current codecept directory (where codecept.json is located).
File will be uploaded to remove system (if tests are running remotely).

```js
I.attachFile('Avatar', 'data/avatar.jpg');
I.attachFile('form input[name=avatar]', 'data/avatar.jpg');
```

**Parameters**

-   `locator`  
-   `pathToFile`  

# checkOption

[lib/helper/Protractor.js:207-220](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L207-L220 "Source code on GitHub")

Selects a checkbox or radio button.
Element is located by label or name or CSS or XPath.

The second parameter is a context (CSS or XPath locator) to narrow the search.

```js
I.checkOption('#agree');
I.checkOption('I Agree to Terms and Conditions');
I.checkOption('agree', '//form');
```

**Parameters**

-   `option`  
-   `context`  

# clearCookie

[lib/helper/Protractor.js:408-413](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L408-L413 "Source code on GitHub")

Clears a cookie by name,
if none provided clears all cookies

```js
I.clearCookie();
I.clearCookie('test');
```

**Parameters**

-   `cookie`  

# click

[lib/helper/Protractor.js:94-100](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L94-L100 "Source code on GitHub")

Perform a click on a link or a button, given by a locator.
If a fuzzy locator is given, the page will be searched for a button, link, or image matching the locator string.
For buttons, the "value" attribute, "name" attribute, and inner text are searched. For links, the link text is searched.
For images, the "alt" attribute and inner text of any parent links are searched.

The second parameter is a context (CSS or XPath locator) to narrow the search.

```js
// simple link
I.click('Logout');
// button of form
I.click('Submit');
// CSS button
I.click('#form input[type=submit]');
// XPath
I.click('//form/*[@type=submit]');
// link in context
I.click('Logout', '#nav');
// using strict locator
I.click({css: 'nav a.login'});
```

**Parameters**

-   `link`  
-   `context`  

# dontSee

[lib/helper/Protractor.js:112-114](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L112-L114 "Source code on GitHub")

Opposite to `see`. Checks that a text is not present on a page.
Use context parameter to narrow down the search.

```js
I.dontSee('Login'); // assume we are already logged in
```

**Parameters**

-   `text`  
-   `context`  

# dontSeeCheckboxIsChecked

[lib/helper/Protractor.js:233-236](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L233-L236 "Source code on GitHub")

 Verifies that the specified checkbox is not checked.
 
**Parameters**

-   `option`  

# dontSeeCookie

[lib/helper/Protractor.js:427-431](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L427-L431 "Source code on GitHub")

Checks that cookie with given name does not exist.
**Parameters**

-   `name`  

# dontSeeCurrentUrlEquals

[lib/helper/Protractor.js:372-376](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L372-L376 "Source code on GitHub")

Checks that current url is not equal to provided one.
If a relative url provided, a configured url will be prepended to it.

**Parameters**

-   `uri`  

# dontSeeElement

[lib/helper/Protractor.js:304-308](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L304-L308 "Source code on GitHub")

Opposite to `seeElement`. Checks that element is not on page.

**Parameters**

-   `locator`  

# dontSeeInCurrentUrl

[lib/helper/Protractor.js:354-358](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L354-L358 "Source code on GitHub")

Checks that current url does not contain a provided fragment.

**Parameters**

-   `urlFragment`  

# dontSeeInField

[lib/helper/Protractor.js:188-190](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L188-L190 "Source code on GitHub")

Checks that value of input field or textare doesn't equal to given value
Opposite to `seeInField`.

**Parameters**

-   `field`  
-   `value`  

# dontSeeInSource

[lib/helper/Protractor.js:322-326](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L322-L326 "Source code on GitHub")

Checks that the current page contains the given string in its raw source code
**Parameters**

-   `text`  

# dontSeeInTitle

[lib/helper/Protractor.js:276-280](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L276-L280 "Source code on GitHub")

Checks that title does not contain text.
**Parameters**

-   `text`  

# executeAsyncScript

[lib/helper/Protractor.js:338-340](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L338-L340 "Source code on GitHub")

Executes async script on page.
Provided function should execute a passed callback (as first argument) to signal it is finished.

**Parameters**

-   `fn`  

# executeScript

[lib/helper/Protractor.js:331-333](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L331-L333 "Source code on GitHub")

Executes sync script on a page.
Pass arguments to function as additional parameters.
Will return execution result to a test.
In this case you should use generator and yield to receive results.

**Parameters**

-   `fn`  

# fillField

[lib/helper/Protractor.js:148-156](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L148-L156 "Source code on GitHub")

Fills a text field or textarea with the given string.
Field is located by name, label, CSS, or XPath.

```js
// by label
I.fillField('Email', 'hello@world.com');
// by name
I.fillField('password', '123456');
// by CSS
I.fillField('form#login input[name=username]', 'John');
// or by strict locator
I.fillField({css: 'form#login input[name=username]'}, 'John');
```

**Parameters**

-   `field`  
-   `value`  

# grabAttribute

[lib/helper/Protractor.js:260-262](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L260-L262 "Source code on GitHub")

Retrieves an attribute from an element located by CSS or XPath and returns it to test.
Resumes test execution, so **should be used inside a generator with `yield`** operator.

```js
let hint = yield I.grabAttributeFrom('#tooltip', 'title');
```

**Parameters**

-   `locator`  
-   `attr`  

# grabCookie

[lib/helper/Protractor.js:438-440](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L438-L440 "Source code on GitHub")

Gets a cookie object by name
* Resumes test execution, so **should be used inside a generator with `yield`** operator.

```js
let cookie = I.grabCookie('auth');
assert(cookie.value, '123456');
```
Returns cookie in JSON [format](https://code.google.com/p/selenium/wiki/JsonWireProtocol#Cookie_JSON_Object).

**Parameters**

-   `name`  

# grabTextFrom

[lib/helper/Protractor.js:241-243](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L241-L243 "Source code on GitHub")

Retrieves a text from an element located by CSS or XPath and returns it to test.
Resumes test execution, so **should be used inside a generator with `yield`** operator.

```js
let pin = yield I.grabTextFrom('#pin');
```

**Parameters**

-   `locator`  

# grabTitle

[lib/helper/Protractor.js:285-290](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L285-L290 "Source code on GitHub")

Retrieves a page title and returns it to test.
Resumes test execution, so **should be used inside a generator with `yield`** operator.

```js
let title = yield I.grabTitle();
```

# grabValueFrom

[lib/helper/Protractor.js:248-255](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L248-L255 "Source code on GitHub")

Retrieves a value from a form element located by CSS or XPath and returns it to test.
Resumes test execution, so **should be used inside a generator with `yield`** operator.

```js
let email = yield I.grabValueFrom('input[name=email]');
```

**Parameters**

-   `locator`  

# resizeWindow

[lib/helper/Protractor.js:445-450](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L445-L450 "Source code on GitHub")

Resize the current window to provided width and height.
First parameter can be set to `maximize`

**Parameters**

-   `width`  
-   `height`  

# see

[lib/helper/Protractor.js:105-107](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L105-L107 "Source code on GitHub")

Checks that a page contains a visible text.
Use context parameter to narrow down the search.

```js
I.see('Welcome'); // text welcome on a page
I.see('Welcome', '.content'); // text inside .content div
I.see('Register', {css: 'form.register'}); // use strict locator
```

**Parameters**

-   `text`  
-   `context`  

# seeCheckboxIsChecked

[lib/helper/Protractor.js:225-228](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L225-L228 "Source code on GitHub")

Verifies that the specified checkbox is checked.

```js
I.seeCheckboxIsChecked('Agree');
I.seeCheckboxIsChecked('#agree'); // I suppose user agreed to terms
I.seeCheckboxIsChecked({css: '#signup_form input[type=checkbox]'});
```

**Parameters**

-   `option`  

# seeCookie

[lib/helper/Protractor.js:418-422](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L418-L422 "Source code on GitHub")

Checks that cookie with given name exists.

```js
I.seeCookie('Auth');
```
**Parameters**

-   `name`  

# seeCurrentUrlEquals

[lib/helper/Protractor.js:363-367](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L363-L367 "Source code on GitHub")

Checks that current url is equal to provided one.
If a relative url provided, a configured url will be prepended to it.
So both examples will work:

```js
I.seeCurrentUrlEquals('/register');
I.seeCurrentUrlEquals('http://my.site.com/register');
```

**Parameters**

-   `uri`  

# seeElement

[lib/helper/Protractor.js:295-299](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L295-L299 "Source code on GitHub")

Checks that element is present on page.
Element is located by CSS or XPath.

```js
I.seeElement('#modal');
```

**Parameters**

-   `locator`  

# seeInCurrentUrl

[lib/helper/Protractor.js:345-349](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L345-L349 "Source code on GitHub")

Checks that current url contains a provided fragment.

```js
I.seeInCurrentUrl('/register'); // we are on registration page
```

**Parameters**

-   `urlFragment`  

# seeInField

[lib/helper/Protractor.js:181-183](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L181-L183 "Source code on GitHub")

Checks that the given input field or textarea equals to given value.
For fuzzy locators, fields are matched by label text, the "name" attribute, CSS, and XPath.

```js
I.seeInField('Username', 'davert');
I.seeInField({css: 'form textarea'},'Type your comment here');
I.seeInField('form input[type=hidden]','hidden_value');
I.seeInField('#searchform input','Search');
```

**Parameters**

-   `field`  
-   `value`  

# seeInSource

[lib/helper/Protractor.js:313-317](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L313-L317 "Source code on GitHub")

Checks that the current page contains the given string in its raw source code.

```js
I.seeInSource('<h1>Green eggs &amp; ham</h1>');
```

**Parameters**

-   `text`  

# seeInTitle

[lib/helper/Protractor.js:267-271](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L267-L271 "Source code on GitHub")

Checks that title contains text.

**Parameters**

-   `text`  

# selectOption

[lib/helper/Protractor.js:119-143](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L119-L143 "Source code on GitHub")

Selects an option in a drop-down select.
Field is siearched by label | name | CSS | XPath.
Option is selected by visible text or by value.

```js
I.selectOption('Choose Plan', 'Monthly'); // select by label
I.selectOption('subscription', 'Monthly'); // match option by text
I.selectOption('subscription', '0'); // or by value
I.selectOption('//form/select[@name=account]','Permium');
I.selectOption('form select[name=account]', 'Premium');
I.selectOption({css: 'form select[name=account]'}, 'Premium');
```

Provide an array for the second argument to select multiple options.

```js
I.selectOption('Which OS do you use?', ['Andriod', 'OSX']);
```

**Parameters**

-   `select`  
-   `option`  

# setCookie

[lib/helper/Protractor.js:392-403](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L392-L403 "Source code on GitHub")

Sets a cookie

```js
I.setCookie({name: 'auth', value: true});
```
Uses Selenium's JSON [cookie format](https://code.google.com/p/selenium/wiki/JsonWireProtocol#Cookie_JSON_Object).

**Parameters**

-   `cookie`  

# waitForClickable

[lib/helper/Protractor.js:464-468](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L464-L468 "Source code on GitHub")

Waits for element to become clickable for number of seconds.

**Parameters**

-   `locator`  
-   `sec`  

# waitForElement

[lib/helper/Protractor.js:455-459](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L455-L459 "Source code on GitHub")

 Waits for element to be present on page (by default waits for 1sec).
 Element can be located by CSS or XPath.
 
**Parameters**

-   `locator`  
-   `sec`  

# waitForText

[lib/helper/Protractor.js:482-489](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L482-L489 "Source code on GitHub")

Waits for a text to appear (by default waits for 1sec).
Element can be located by CSS or XPath.
Narrow down search results by providing context.

```js
I.waitForText('Thank you, form has been submitted');
I.waitForText('Thank you, form has been submitted', 5, '#modal');
```

**Parameters**

-   `text`  
-   `sec`  
-   `context`  

# waitForVisible

[lib/helper/Protractor.js:473-477](https://github.com/Codeception/CodeceptJS/blob/9872e79fe65ee3473c0c6d1bbae0b78a7601ec3a/lib/helper/Protractor.js#L473-L477 "Source code on GitHub")

Waits for an element to become visible on a page (by default waits for 1sec).
Element can be located by CSS or XPath.

**Parameters**

-   `locator`  
-   `sec`  
