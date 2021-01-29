<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [ngx-tansu](./ngx-tansu.md)

## ngx-tansu package

## Classes

|  Class | Description |
|  --- | --- |
|  [DerivedStore](./ngx-tansu.derivedstore.md) |  |
|  [Store](./ngx-tansu.store.md) | Base class that can be extended to easily create a custom [Readable](./ngx-tansu.readable.md) store. |

## Functions

|  Function | Description |
|  --- | --- |
|  [derived(stores, deriveFn)](./ngx-tansu.derived.md) | A convenience function to create a new store with a state computed from the latest values of dependent stores. Each time the state of one of the dependent stores changes, a provided derive function is called to compute a new, derived state. |
|  [derived(stores, deriveFn, initialValue)](./ngx-tansu.derived_1.md) |  |
|  [get(store)](./ngx-tansu.get.md) | A utility function to get the current value from a given store. It works by subscribing to a store, capturing the value (synchronously) and unsubscribing just after. |
|  [readable(value, onUseFn)](./ngx-tansu.readable.md) | A convenience function to create [Readable](./ngx-tansu.readable.md) store instances. |
|  [writable(value, onUseFn)](./ngx-tansu.writable.md) | A convenience function to create [Writable](./ngx-tansu.writable.md) store instances. |

## Interfaces

|  Interface | Description |
|  --- | --- |
|  [OnUseArgument](./ngx-tansu.onuseargument.md) |  |
|  [Readable](./ngx-tansu.readable.md) | This interface augments the base [SubscribableStore](./ngx-tansu.subscribablestore.md) interface with the Angular-specific <code>OnDestroy</code> callback. The [Readable](./ngx-tansu.readable.md) stores can be registered in the Angular DI container and will automatically discard all the subscription when a given store is destroyed. |
|  [SubscribableStore](./ngx-tansu.subscribablestore.md) | Represents a store accepting registrations (subscribers) and "pushing" notifications on each and every store value change. |
|  [SubscriberObject](./ngx-tansu.subscriberobject.md) | A partial \[observer\](https://github.com/tc39/proposal-observable\#api) notified when a store value changes. A store will call the <code>next</code> method every time the store's state is changing. |
|  [UnsubscribeObject](./ngx-tansu.unsubscribeobject.md) | An object with the <code>unsubscribe</code> method. Subscribable stores might choose to return such object instead of directly returning [UnsubscribeFunction](./ngx-tansu.unsubscribefunction.md) from a subscription call. |
|  [Writable](./ngx-tansu.writable.md) | Builds on top of [Readable](./ngx-tansu.readable.md) and represents a store that can be manipulated from "outside": anyone with a reference to writable store can either update or completely replace state of a given store.
```typescript
// reset counter's store value to 0 by using the {@link Writable.set} method
counterStore.set(0);

// increment counter's store value by using the {@link Writable.update} method
counterStore.update(currentValue => currentValue + 1);

```
 |

## Type Aliases

|  Type Alias | Description |
|  --- | --- |
|  [Subscriber](./ngx-tansu.subscriber.md) | Expresses interest in store value changes over time. It can be either: - a callback function: [SubscriberFunction](./ngx-tansu.subscriberfunction.md)<!-- -->; - a partial observer: [SubscriberObject](./ngx-tansu.subscriberobject.md)<!-- -->. |
|  [SubscriberFunction](./ngx-tansu.subscriberfunction.md) | A callback invoked when a store value changes. It is called with the latest value of a given store. |
|  [UnsubscribeFunction](./ngx-tansu.unsubscribefunction.md) | A function to unsubscribe from value change notifications. |
|  [Unsubscriber](./ngx-tansu.unsubscriber.md) |  |
|  [Updater](./ngx-tansu.updater.md) | A function that can be used to update store's value. This function is called with the current value and should return new store value. |
