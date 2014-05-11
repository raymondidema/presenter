# View Presenters

## Usage

### Presenters
```
    use Raymondidema\Presenter\Presenter;
    class UserPresenter extends Presenter {
        public function fullName()
        {
            return $this->first . ' ' . $this->last;
        }
    }
```

### Models

```
    use Raymondidema\Presenter\PresentableTrait;

    class User extends \Eloquent {
        use PresentableTrait;
        protected $presenter = 'UserPresenter';
    }
```

## How to use

```
    <h1>Hello, {{ $user->present()->fullName }}.</h1>
```

