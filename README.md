# Драйвер для ввода символов с помощью компьютерной мыши
Курсовая работа по операционным системам. 7 семестр ИУ7 МГТУ им. Баумана.

По сути единственный приятный момент во всём курсе операционных систем был, когда этот драйвер заработал. Я испытал реальный кайф) Правда потом было изготовление РПЗ и 1.5 недели её сдачи, но не суть.

Сдача пошла поперёк. Мне не повезло, Рязанова 3 раза надиктовывала правки в РПЗ. Последние я хотел внести, сидя у неё на паре на следующий день. Но когда пришёл, она меня увидела и сказала: "Я думала о твоём курсовом, поняла, что драйвер тебе не нужен, ты обманщик, иди печатай РПЗ, поставлю 4". Ок...


То, что реализовано в этом курсаче - по сути велосипед, вклинивание в подсистему ввода и собственная запись структур событий в event-файлы. Причем работает этот велосипед только до определённой версии ядра. На 5.11.0 функция kernel_write не умеет работать с event-файлами. Почему - хз. Смог найти только единственное [ишью](https://github.com/openzfs/zfs/issues/11445) с на похожую тему, но как это решать, там не описывается. Поэтому сдавал на 5.4.50, там работает нормально. 

Уже после сдачи своего курсового узнал, что в ядре для этого есть нормальное API. Дописывать вряд ли буду. Необходимые материалы есть в книге Essential Linux Device Drivers. Вот [ссылка](http://dmilvdv.narod.ru/Translate/ELDD/Essential_Linux_Device_Drivers_ru.pdf) на перевод нужного куска.

А так, не парьтесь. Вы уже закрыли оба семестра по ОСам. Хотя бы тройку Наталья Юрьевна, да поставит. Многим этого достаточно. Для этого можно скатать какую-нибудь попсовую тему, а не запариваться как я. Удачи, ребят.
