### Code-review-checklist

#### Code
1. Check android lint(Analyze -> Inspect Code): https://developer.android.com/studio/write/lint.
2. Check memory leak(Profiler. Tutorial: https://www.youtube.com/watch?v=58HNvOGx16Q).
3. Check Kotlin style guide: https://developer.android.com/kotlin/style-guide. (https://github.com/RedMadRobot/kotlin-style-guide)
4. Apply style guide: https://kotlinlang.org/docs/coding-conventions.html#configure-style-in-ide.
5. Check naming conversions: !!! Finishing
6. Check gitignore.
7. 


#### UI
1. OnClick view with animation.
2. Not a small click area - use padding.
3. Hide/show view with animation.
4. Work with list(RecyclerView) with animation (use DiffUtils).
5. 


Сессия №3
Kotlin
 - Функциональное ОО програмирование: как применяем в Котлине?
 - Какой опыт работы с Kotlin.
 - Различия между модификаторами доступа и модификаторами видимости?
 - open
 - В каких случаях используем final
 - Типы данных в Kotlin. Особенности (Примитивы, мутабле иммутабле, nullsafe)
 - Отличие примитивов от ссылочных типов.
 - Иерархия типов (Базовые класс (Any, Nothing, Unit)
 - Особенност Object
 - Аналог void в Котлин?
 - Как работают extention fun. Как в Java бы делал.
 - Можно ли в Kotlin получить nullpointer exception. (При взаимодействии с Java)
 - Типы конструкторов в Котлин. В чем отличия.
 - Чем конструктор в Java отличается от обычной функции.
 - Sealed и Enum класс: отличия и сходства.
 - Вложенный и внутренний класс: отличия и сходства.
 - Что такое data класс и где используем?
 - Чем дата класс отличается от обычного класса?
 - Компоненты data class'а?
 - Delegate. Виды делегатов.
 - Примеры делегатов свойств.
 - Как делегаты свойств под капотом работают. Их особенности.
 - Если взять обычный геттер и сеттер и взять делегат. Что лучше по памяти/скорости.
 - Рефлексия.
 - Корутины. В чем отличие корутин от потоков. В чем киллер фича корутин?
 - Отличия многопоточной операции от асинхронной.
 - Inline function.
 - Infix function.
 - Чем объявление константы отличается от объявления обычной переменной?
 - С inline анонимный класс не будет создан?
 - Value class.
 - Типы ссылок(сильные, слабые, фантомные). В каких случаях их используем.

 - Отличия коллектции от сиквелс (в плане работы с операторами)
 - Что происходит и в чем отличия:
1. object : Runnable {
     override fun run() {
     }
 }
2. Runnable { }

1. listOf(...).filter {}.map {}.take{}
2. listOf(...).asSequence().filter {}.map {}.take{}.toList()

Написать реализацию:
val numbers: List<Int> = listOf(4, 2, 3, 4, 5).filter{it-> it==4}

Задача от Сани: 
Есть 3 потока. Они работают с одной переменной. Последовательно увеличивают её значение. В один момент мы печатаем эту переменную во всех потока. Какой будет значение?








Сессия №2
Android
 - Зачем нужен манифест? Кто его использует?
 - Компоненты андроид приложения.
 - ЖЦ активити. Когда вызываются методы ЖЦ. Что мы делаем в этих методах.
 - Гарантированн ли вызов всех этих методов.
 - Создание активити в разных процессах.
 - Context activity - что это такое и зачем использовать?
 - Отличия activity context and application context. В каких случаях использовать.
 - В каких ещё ситуациях активити уничтожается. (поворот и смена конфигурации)
 - Сохранение состояние при повороте экрана?
 - Как долго живет bundle из acrivity.onCreate(savedInstanceState: Bundle)
 - До какого момента ViewModel гарантирует сохранение состояния? (Пока жив процесс)
 - Отличия bundle от VM.
 - Launch Modes for activity (standart, singleTop, singleTask, singleInstance)
 - Service и Активити: что общего и в чем различия.
 - Чем отличается Background Service от Foreground.
 - Если убить приложение, сервис будет работать
 - Приоритеты задач. Что приоритетнее Background Service или Foreground.
 - Есть привязанные сервисы, а есть запущенные. Чем они отличаются?
 - В каком потоке работает Service? Как для него создать второй поток?
 - IntentService и JobIntentService в чем разница?
 - Почему IntentService deprecated?
 - Планировщики задач: WorkManager JobSchedule: когда используем первый/второй.
 - Чем Worker отличается от Service?
 - Различия между Notification and PushNotification.
 - Как с уведомления перейти на нужный экран: активити/фрагмент (Deep link).
 - Intent для чего используется. Чем явный интент отличается от неявного.
 - Можно ли передавать в bundle объект.
 - Сериализация в андроид: Serializable and Parcelable: что использовать и зачем?
 - Что такое фрагменты? Зачем они создавалсь и как сейчас мы их используем.
 - ЖЦ фрагмента.
 - Почему есть 2 метода onCreate and onCreateView (retain instanse fragment)
 - Почему используем bundle для передачи данных, а не конструктор фрагмента?
 - Зачем ContentProvider.
 - FileProvide vs. ContentProvider.
 - Зачем BroadcastReceiver.
 - Анимация в андроид.
 - Отличия RecyclerVIew vs. ListView.
 - Как работает Diff Util. Зачем нужны 2 метода.
 - Зачем нужны исключения? Иерархия исключений.
 - Что такое утечка памяти? Как отследить утечку? Profiler
 - Java memory model. Gc roots.
 - Как работает сборщик мусора? В какой момент запускается.
 - Есть разные layouts. В каких ситуация какой layout использовать.
 - CustomView ЖЦ.
 - Отличия invalidate() от requestLayout?Форсе лайоут
 - Difference between View.GONE and View.INVISIBLE?
 - Многопоточность. Evolution of Thread.
 - Зачем нужен Handler.
 - Looper, Handler and HandlerThread, Thread Pool, Executor
 - SOLID
 - Отличия Assets от Raw. Drawable vs. Mipmap.
 - Постоянное хранение данных. С чем работал.
 - Может ли пользователь стереть базу.
 - Что такое SharedPeferencess?
 - В каком потоке работает SP?
 - Зачем нужен мультидекс?
 - Data binding vs. View binding
Задача: Отправить отчет на сервер, отчет большой, весит гигабайты, интернет не быстрый. Как делать? Человек заполняет большой и тяжелый отчет, нажимает кнопку отпавить, и кладет телефон в карман.
Сессия №6
Data Structures
 - ArrayList vs Array
 - ArrayList vs MutableList
 - ArrayList от LinkedList
 - Что такое сложность?
 - Сложность вставки в середину?
 - Если ограниче по память на телефоне, что использовать оптимальнее?
 - Как миним. всплеск/затраты памяти, при работе с AL? (Задавать начальное капасити)
 - В каких случаях используем то или это?
 - Vector vs Stack
 - Queue vs Deque
 - Зачем HashSet?
 - LinkedHashSet vs TreeSet
 - ArraySet vs HashSet
ЗАДАЧА
 - Принцип работы HashMap, реализация
 - Если использовать в качестве ключа объект и потом изменять его
 - В контексте: зачем использовать только val data class.

Задача:
Нужно сделать игру сапер. На экране есть ячейки. При старте рандомно генерируются заминированные ячейки. Какая в целом схема работы? Какие структуры данных использовать?
