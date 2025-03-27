### Список тем для прокачки Middle iOS-разработчика

#### 1. Многопоточность и Concurrency
- **Основы многопоточности**: [[Session 14. Многопоточка]] (Podlodka) — понимание потоков, очередей и их применения.
- **Async/Await**: 
  - [AsyncAwait Василий Усов](https://www.youtube.com/watch?v=DIDoHx6KP50&t=1889s) — освоение современной конкурентности в Swift.
  - [Swift async/await. Чем он лучше GCD?](https://habr.com/ru/articles/727788/) — сравнение с GCD.
  - [Task и structured concurrency в Swift](https://habr.com/ru/articles/762148/) — структурированная конкурентность.
- **GCD и альтернативы**: 
  - [Dispatch Semaphore](https://riptutorial.com/ios/example/28284/dispatch-semaphore) — управление доступом к ресурсам.
  - [Operation and OperationQueue Tutorial in Swift](https://www.kodeco.com/5293-operation-and-operationqueue-tutorial-in-swift) — работа с операциями.
- **Алгоритмы конкурентности**: [алгоритмы AsyncAwait](https://github.com/apple/swift-async-algorithms) — практическое применение.

#### 2. Управление памятью
- **ARC и основы**: 
  - [Управление памятью в Swift](https://habr.com/ru/articles/592385/) — как работает ARC.
  - [Advanced iOS Memory Management with Swift: ARC, Strong, Weak and Unowned Explained](https://www.vadimbulavin.com/swift-memory-management-arc-strong-weak-and-unowned/) — глубокое погружение в ссылочные типы.
- **Stack vs Heap**: [Stack vs Heap Memory Allocation](https://net-informations.com/faq/net/stack-heap.htm) — различия и применение.
- **Диагностика проблем**: 
  - [EXC_BAD_ACCESS](https://www.avanderlee.com/swift/exc-bad-access-crash/) — разбор типичных ошибок.
  - [The Hidden Treasures of Crash Reports](https://objective-see.org/blog/blog_0x7B.html) — анализ краш-репортов.

#### 3. SwiftUI
- **Основы и продвинутые техники**: 
  - [Рисование в SwiftUI. Image. Canvas](https://twocentstudios.com/2025/03/10/pixel-art-swift-ui/) — работа с графикой.
  - [Navigation Stack in SwiftUI](https://vk.com/@-224142498-navigationstack-2023) — управление навигацией.
  - [Фон для List в SwiftUI](https://sarunw.com/posts/swiftui-list-background-color/) — кастомизация интерфейсов.
- **Анимации**: 
  - [Инкубатор. Анимация SUI](https://www.youtube.com/live/9GDZDxBEw2E?si=V8DW2sk9hcD-oWkp) — базовые анимации.
  - [SwiftUI эффекты](https://github.com/EmergeTools/Pow?tab=readme-ov-file) — продвинутые эффекты.
  - [Анимация SwiftUI](https://www.youtube.com/watch?v=FtDy9UkhbjY) — практические примеры.
- **Интеграция с UIKit**: [[Как смиксовать навигацию UIKit и SUI]] — гибридные приложения.

#### 4. UI и визуализация
- **UIScrollView**: [[Как работает UIScrollView]] — механика работы и оптимизация.
- **CALayer и анимации**: 
  - [Advanced animation CALayer](https://www.youtube.com/watch?v=PY40m0JXLL8) — продвинутая работа с слоями.
  - [Tiled Layer Example](https://github.com/gregoryvit/podlodka-crew-tiled-layer) — оптимизация больших изображений.
- **UICollectionView**: 
  - [UICollectionView. Layout](https://www.youtube.com/watch?v=yBnxUAOIsYE) — кастомные布局.
  - [Доклад подлодки-13. UICollectionView](https://github.com/alexfilimon/uicollectionviewlayout-example) — примеры реализации.

#### 5. Metal и графика
- **Введение в Metal**: 
  - [Подлодка. Кузница пикселей: Как запечь Metal на GPU и не обжечься](https://www.youtube.com/watch?v=uuwSNGQlFak) — основы работы с GPU.
  - [Курс по Metal для новичков](https://www.youtube.com/watch?v=TEqbZ7Ai7AA&list=PL23Revp-82LJG3vcDPm8w7b5HTKjBOY0W) — пошаговое обучение.
- **Шейдеры**: 
  - [Шейдеры в iOS для начинающих](https://habr.com/ru/companies/dododev/articles/759574/) — базовые шейдеры.
  - [Линк про шейдеры](https://www.shadertoy.com/view/XsXXDn) — примеры.

#### 6. Работа с данными
- **SwiftData и Core Data**: 
  - [Шпаргалка по Core Data для Swift разработчиков на iOS](https://medium.com/@SwiftBook.ru/шпаргалка-по-core-data-для-swift-разработчиков-на-ios-9dce9b1c610d) — основы Core Data.
  - [Как работать со Swift Data и Core Data в фоновом режиме](https://www.polpiella.dev/core-data-swift-data-concurrency/) — конкурентность.
  - [Большой гайд по работе с SwiftData](https://t.me/iosdev/1153) — углубленное изучение.
- **Combine**: [Гид по Combine](https://tanaschita.com/combine-essentials/) — реактивное программирование.

#### 7. Оптимизация и производительность
- **Method Dispatch**: 
  - [Method Dispatch in Swift](https://trinhngocthuyen.com/posts/tech/method-dispatch-in-swift/) — понимание диспетчеризации.
  - [Диспетчеризация методов в Swift](https://habr.com/ru/articles/714830/) — теория и практика.
- **Профилирование**: 
  - [TimeProfiler оптимизация UI](https://www.youtube.com/watch?v=C9ylmurvK_o) — анализ производительности UI.
  - [Андрей Акиньшин - Поговорим про перформанс-анализ](https://www.youtube.com/watch?v=gc3yVybPuaY) — инструменты и подходы.

#### 8. Тестирование
- **Swift Testing**: [[Swift Testing]] — современный подход к тестированию в Swift.
- **Практика**: Изучение написания юнит-тестов и UI-тестов на основе материалов.

#### 9. Инструменты и процессы
- **Xcode**: 
  - [Система сборки Xcode](https://www.vadimbulavin.com/xcode-build-system/) — понимание сборки.
  - [Как происходит компиляция в Xcode](https://www.youtube.com/watch?v=bEXwEeBV_U4) — процесс компиляции.
- **Tuist**: [[Tuist]] — управление проектами и зависимостями.

#### 10. Дополнительные навыки
- **Алгоритмы**: [Swift Algorithm Club](https://github.com/kodecocodes/swift-algorithm-club/tree/master/Linked%20List) — базовые структуры данных.
- **Работа с датой и временем**: [Доклад. Дата и время в Swift](https://www.youtube.com/watch?v=mZ9HNSApGJI) — правильная обработка.
- **Embedded Swift**: [[Embedded Swift]] — работа с ограниченными ресурсами.

---

### Рекомендации по изучению
1. **Фокус на практике**: После каждой темы старайтесь написать небольшой проект или решить задачу (например, шахматы на SwiftUI из [Разработка шахмат на SwiftUI](https://danielraffel.me/til/2024/11/13/how-to-set-up-a-local-ai-model-with-xcode-ollama-qwen2-5-coder-alex-sidebar/)).
2. **Приоритет**: Начните с многопоточности (Async/Await), управления памятью и SwiftUI — это ключевые навыки для middle-разработчика.
3. **Глубина**: Для каждой темы изучайте не только статьи, но и код (например, репозитории на GitHub).
4. **Собеседования**: Используйте [[Вопросы по SUI прокачка к собесам]] для подготовки к техническим интервью.