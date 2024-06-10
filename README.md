# SilverStripe 5 Duplicate DataObject

Adds a duplicate button to GridField in the CMS that enables duplicating of dataobjects.

Forked from [jinjie/duplicate-dataobject](https://github.com/jinjie/duplicate-dataobject) and updated to support SS5.

## Installation 

``composer require roseblade/ss-duplicate-dataobject``

## Usage Example

This module uses the built in DataObject duplication.

See

- https://api.silverstripe.org/4/SilverStripe/ORM/DataObject.html#method_duplicate
- https://docs.silverstripe.org/en/4/developer_guides/model/relations/#cascading-duplications

```php
// Add component on existing GridField
$fields->fieldByName('Root.Main.MyGridField')
    ->getConfig()
    ->addComponent(new GridFieldDuplicateAction());

// Add component on new GridField
$fields->push(
    GridField::create(
        'MyGridField',
        'MyGridField'
    )->addComponent(new GridFieldDuplicateAction())
);
```

## Author

Developed by Jin Jie @ [Swift DevLabs](https://www.swiftdev.sg/) 
