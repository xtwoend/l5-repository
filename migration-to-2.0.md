# Laravel 5 Repositories

## Migrate from version 1.0 to 2.0

### Registering the model's repository

*Versão 1.0*

```php
use Prettus\Repository\Eloquent\Repository;

class PostRepository extends Repository {

    public function __construct(Post $model)
    {
        parent::__construct($model);
    }   
    
}
```

*Versão 2.0*

```php
use Prettus\Repository\Eloquent\BaseRepository;

class PostRepository extends BaseRepository {
    
    /**
     * Specify Model class name
     *
     * @return string
     */
    function model()
    {
        return "App\\Post";
    }
}
```