# onClose
## Description:
```php
callback Worker::$onClose
```

Emitted once the connection is closed.

## Parameters

``` $connection ```

The instance of Connection.


## Examples

```php
use Workerman\Worker;
require_once './Workerman/Autoloader.php';

$worker = new Worker('websocket://0.0.0.0:8484');
$worker->onClose = function($connection)
{
    echo "connection closed\n";
};

// Run all workers
Worker::runAll();
```
