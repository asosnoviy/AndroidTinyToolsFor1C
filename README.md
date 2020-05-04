Внешняя компонента добавляет следующий функционал:

1. Возможность подписки на прием широковещательных оповещений. При получении оповещения, вызывается обработчик события ВнешнееСобытие у всех открытых форм.

Запуск подписки:

AndroidTools.StartBroadcastReceiver(<ИмяСобытия>, <ИмяПараметра>);

где,

<ИмяСобытия> - имя события, на которое устанавливается подписка.

<ИмяПараметра> - имя параметра, в котором будут содержаться полученные данные события.
 

Пример:

AndroidTools.StartBroadcastReceiver("com.google.android.c2dm.intent.RECEIVE", "data");

Важно чтобы переменная с объектом компоненты (AndroidTools) была глобальной в модуле формы, поскольку подписка будет работать до тех пор, пока переменная остается в памяти.

2. Вибрация

AndroidTools.Vibrate([<Длительность вибрации в миллисекундах>]);

По умолчанию, длительность вибрации - 500 миллисекунд.

3. Воспроизведение короткого сигнала

AndroidTools.Beep([<Код сигнала>]);

где

Код сигнала- Числовая константа, определяющая то, какой именно звуковой сигнал будет проигран. По умолчанию = TONE_PROP_BEEP = 24.

Доступные значения можно посмотреть в Android SDK, у класса ToneGenerator.
 

4. Toast - всплывающее стандартное окно сообщений. Окно появляется на короткое время и затем исчезает.

AndroidTools.Toast("Привет!");

 

