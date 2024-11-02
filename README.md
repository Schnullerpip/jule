# @fettstorch/jule

A collection of TypeScript utilities I use in my projects.

## Installation

Using bun:
```bash
bun add @fettstorch/jule
```

## Usage examples

### when
```ts
import { when } from '@fettstorch/jule'
function foo(case: number): string {
    return when(case)({
        1: () => 'one',
        2: () => 'two',
        else: () => 'something else'
    })
}
```

### awaitable
```ts
import { awaitable } from '@fettstorch/jule'
const { promise, resolve } = awaitable()
```

### Observable
```ts
import { Observable } from '@fettstorch/jule'
const observable = new Observable<number>()
observable.subscribe(value => console.log(value))
observable.emit(1)
```

### once
```ts
import { once } from '@fettstorch/jule'
const computationHeavyStuff = once(() => computationHeavyStuff())
```

### Once
```ts
import { Once } from '@fettstorch/jule'
class TestClass {
    @Once
    get foo() {
        const result = computationHeavyStuff()
        return 1
    }
}
```
