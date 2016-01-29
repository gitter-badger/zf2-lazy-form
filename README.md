Lazy Form for Zend Framework 2
=============
Developed by Ibrahim Azhar Armar

Introduction
------------
Did you ever get frustrated by the fact that you have to repeat the same validators, filters, attributes and options over and over again in different forms and elements leading to code duplication and maintenance nightmare ? we have read numerous time about [DRY - Don't repeat yourself](https://en.wikipedia.org/wiki/Don't_repeat_yourself) or [OAOO - Once and Only Once](http://c2.com/cgi/wiki?OnceAndOnlyOnce), the question is do we really follow it ?

Zf2LazyForm module was developed to eliminate duplication and encourage reuse. during the course of development we enhanced the module to support numerous features.
* Reusable and configurable validators, filters, attrbutes, options
* Short and easy syntax
* Define global form elements and attributes

Let's get started by first installing the module in your ZF2 application.

#### Install using composer
```
composer require oromedialab/zf2-lazy-form dev-master
```

#### Install using GIT clone
```
git clone https://github.com/oromedialab/zf2-lazy-form.git
```

#### Enable Zf2 Module
Enable the module by adding `Oml\Zf2LazyForm` in your `config/application.config.php` file.

Now that you have installed and enabled some module, lets try creating a simple form element

```php
use Oml\Zf2LazyForm\Form\Base;

class MyForm extends Base
{
	public function __construct($name = null)
	{
		parent::__construct(null);

		$this->addFormElement(['name' => 'name', 'label' => 'Name', 'type' => 'text']);
	}
}
```

That's it, it added a form element of type text in your form.