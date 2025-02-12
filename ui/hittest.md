# HitTest


- 🟧 [HitTest статья Medium](https://medium.com/yandex-maps-mobile/держим-удар-с-hittest-542653d51a8c)
- 🟧 [Hit-testing in iOS](https://smnh.me/hit-testing-in-ios)

### Краткое содержание статьи "Держим удар с hitTest"

**Основные методы:**
1. **hitTest(_:with:)**

```swift
override func hitTest(_ point: CGPoint, with event: UIEvent?) -> UIView? {
    guard isUserInteractionEnabled else { return nil }
    guard !isHidden else { return nil }
    guard alpha >= 0.01 else { return nil }
    guard point(inside: point, with: event) else { return nil }
    
    for subview in subviews.reversed() {
        let convertedPoint = subview.convert(point, from: self)
        if let hitView = subview.hitTest(convertedPoint, with: event) {
            return hitView
        }
    }
    return self
}
```
**Описание:** Метод определяет, какая вью иерархии должна получить событие касания.

2. **point(inside:with:)**

```swift
override func point(inside point: CGPoint, with event: UIEvent?) -> Bool {
    let inside = super.point(inside: point, with: event)
    if !inside {
        for subview in subviews {
            let pointInSubview = subview.convert(point, from: self)
            if subview.point(inside: pointInSubview, with: event) {
                return true
            }
        }
    }
    return inside
}
```
**Описание:** Проверяет, находится ли точка касания внутри вью или её подвидов.

### Основные моменты:

1. **Обработка касания:** События касания создаются и передаются через `UIApplication`, который направляет их в `UIWindow`.
2. **Рекурсивный поиск:** Метод `hitTest` рекурсивно ищет самую глубокую вью, соответствующую точке касания.
3. **Игнорирование кликов:** Если точка касания вне границ вью, она и её подвиды игнорируются.

Эти методы используются для точного определения получателя событий касания в иерархии вью, что позволяет реализовать сложные пользовательские взаимодействия и интерфейсы.

--- 
Однако, я могу рассказать о ключевых методах, связанных с обработкой жестов и событий в iOS, основанных на использовании методов `hitTest` и `pointInside`.

### Ключевые методы:

1. **hitTest(_:with:)**

```swift
override func hitTest(_ point: CGPoint, with event: UIEvent?) -> UIView? {
    if !self.isUserInteractionEnabled || self.isHidden || self.alpha <= 0.01 {
        return nil
    }
    
    if self.point(inside: point, with: event) {
        for subview in self.subviews.reversed() {
            let convertedPoint = subview.convert(point, from: self)
            if let hitTestView = subview.hitTest(convertedPoint, with: event) {
                return hitTestView
            }
        }
        return self
    }
    return nil
}
```
**Описание**: Этот метод определяет, какой вью должен получать событие касания. Он сначала проверяет, может ли вью обрабатывать взаимодействия, затем проверяет, находится ли точка касания внутри границ вью. Если да, он рекурсивно проверяет подвиды (subviews) вью. Если ни один из подвидов не подходит, текущая вью возвращается как получатель события.

2. **pointInside(_:with:)**

```swift
override func point(inside point: CGPoint, with event: UIEvent?) -> Bool {
    return self.bounds.contains(point)
}
```
**Описание**: Этот метод проверяет, находится ли точка касания внутри границ вью. Это помогает определить, следует ли учитывать эту вью для получения событий касания.

### Пример последовательности обработки событий:

1. **Касание экрана**: Пользователь касается экрана, создается событие `UIEvent`.
2. **Определение получателя**: Событие передается в корневую вью, которая вызывает метод `hitTest(_:with:)`.
3. **Рекурсивная проверка**: `hitTest(_:with:)` рекурсивно проверяет все подвиды, вызывая метод `pointInside(_:with:)` для каждой вью, чтобы определить, находится ли точка касания внутри нее.
4. **Назначение получателя**: Как только соответствующая вью найдена, она назначается получателем события и обрабатывает его.

Эти методы играют ключевую роль в системе обработки событий iOS, позволяя точно определять, какая вью должна получать и обрабатывать касания пользователя.
