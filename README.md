# rxjs-exhaustmap-with-trailing

A variant of RxJS exhaustMap that includes trailing emissions from the source observable.

Just like the `exhaustMap()` RxJS operator, `exhaustMapWithTrailing()` will ignore all emissions from source observable as long as the projected observable is pending, but in addition it will include the last emission received from the source observable received before the projected observable completed. Think of it as a combination of `exhaustMap()` and `debounce()`.

## Usage

```js
import {exhaustMapWithTrailing} from "rxjs-exhaustmap-with-trailing"
import {fromEvent, interval} from "rxjs"

const clicks = fromEvent(document, "click")
const result = clicks.pipe(
  exhaustMapWithTrailing((event) =>
    interval(1000).pipe(mapTo({clientX: event.clientX, clientY: event.clientY}))
  )
)
result.subscribe((x) => console.log(x))
```

## API

### exhaustMapWithTrailing
```
exhaustMapWithTrailing<T, R>(project: (value: T, index: number) => ObservableInput<R>): OperatorFunction<T, R>;
```

### exhaustMapToWithTrailing
```
exhaustMapToWithTrailing<T, R>(innerObservable: Observable<R>): OperatorFunction<T, R>;
```

## Credits

This is a packaged and unit tested version of the implementation posted by @aaronjensen here: https://github.com/ReactiveX/rxjs/issues/5004
