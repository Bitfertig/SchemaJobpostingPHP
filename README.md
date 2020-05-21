# SchemaJobpostingPHP


## Download

https://github.com/Bitfertig/SchemaJobpostingPHP


## Usage

First include the jobposting php class.

```php
<?php include_once 'path/to/schema-jobposting.class.php'; ?>
```

Then use the class on your site to generate JSON-format or a script.

```php
<?php
$sjp = new SchemaJobposting();
$sjp->set('datePosted', '');
$sjp->set('validThrough', date('Y-m-d', strtotime('+1 year')));
$sjp->set('title', '');
$sjp->set('description', '');
$sjp->set('employmentType', []); // FULL_TIME, PART_TIME, contract, temporary, seasonal, internship
$sjp->set('hiringOrganization.name', '');
$sjp->set('hiringOrganization.sameAs', '');
$sjp->set('hiringOrganization.logo', '');
$sjp->set('jobLocation.address.streetAddress', '');
$sjp->set('jobLocation.address.addressLocality', '');
$sjp->set('jobLocation.address.postalCode', '');
$sjp->set('jobLocation.address.addressRegion', ''); // adressRegion (Land-Bundesland als ISO 3166-2 Code) https://de.wikipedia.org/wiki/ISO_3166-2
$sjp->set('jobLocation.address.addressCountry', '');
$sjp->set('baseSalary.currency', 'EUR');
$sjp->set('baseSalary.value', 'nach Vereinbarung / Qualifikation');
//echo '<pre><mark>|'.$sjp->toJson();echo '|</mark></pre>';
echo $sjp->toScript();
?>
```

You can add more with this dot notation.


### Development

Convert Markdown to HTML with https://cloudconvert.com/md-to-html