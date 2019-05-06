# Ongoing

This package includes (php)-classes for [Ongoing Warehouse](http://ongoingwarehouse.se/)'s Soap-api. 

The classes are generated with [Wsdl2phpgenerator](https://github.com/wsdl2phpgenerator/wsdl2phpgenerator). When Ongoing updates their api the classes can be updated with `php generate.php https://api.ongoingsystems.se/apidemo/service.asmx?WSDL`.

## Install with composer
`composer require starweb/ongoing`

## Example
```php
$service = new \Ongoing\Service([], 'https://api.ongoingsystems.se/apidemo/service.asmx?WSDL');
$getOrderByOrderNumber = new \Ongoing\GetOrderByOrderNumber($goodsOwnerCode, $username, $password, $orderNumber);
$order = $service->GetOrderByOrderNumber($getOrderByOrderNumber)->getGetOrderByOrderNumberResult();
```

