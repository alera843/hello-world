# hello-world
just a repository

СКРИВАНЕ НА ИНФОРМАЦИЯ ОТ ПРОИЗВОЛЕН ТИП В ЦИФРОВИ ИЗОБРАЖЕНИЯ
АВГУСТ 17, 2018 ДЕНИС ТОПОВ
Автор: инж. Христо Трифонов Терзиев

С непретенциозен софтуер може да се скрие всеки файл (включително .exe) в обикновено изображение във формат JPEG

 

ИНФОРМАЦИОННА СИГУРНОСТ

Понятието информация е толкова разпространено като смисъл и употреба и може да бъде дефинирано по различни начини. В най-тесен и конкретен смисъл информацията представлява съвкупност от символи, притежаващи определен смисъл. В широк контекст информацията може да бъде представена като знание, идеи и т.н.

Гарантирането на тайната, целостта и наличността на информацията не е загубила своята актуалност от древността. С откриването на всеки нов способ за предаване на информация още от древни времена се раждали и нови идеи за скриване на секретни съобщения. Един от ефективните подходи за защитата на важна информация е скриването на съществуването ѝ. За най-ефективно постигане на това са се оформили две основни направления. Методите на първото направление са скривали съдържанието на съобщенията чрез използване на шифри и дават началото на класическата криптография. Второто направление е скривало самото съществуване на такава информация при нейното съхраняване или предаване, чрез много техники и средства.

СТЕГАНОГРАФИЯ

Знанията и техническите умения през вековете за скриване на наличието на тайни съобщения, се обособили в научно-приложна област, наречена днес стеганография. Терминът „стеганография“ произлиза от две гръцки думи – steganos (тайно) и graphy (писмено) и може да се преведе на български език като „тайнопис”.Техниките за скриване на информация са наречени стеганографски методи. Стеганографска система или стегосистема е съвкупност от средства и методи, които се използват за формиране на скрит канал за предаване на информация.

Стеганографията като подход за защита на информацията се използва за скриването ѝ в обект контейнер, като по този начин съществуването на самата комуникация е неоткриваемо за разлика от криптографията, където съществуването на тайна комуникация е известно, но е неразгадаемо. Тоест за разлика от криптографията, която крие съдържанието на тайно послание, стеганографията крие самото съществуване.

Докато криптографията опира до стабилни познания по математика, стеганографията изисква не само математически познания, но и голяма степен въображение, нестандартни идеи и много оригиналност за скриването на информация в друга. Един такъв подход за скриване на данни е методът RARJPEG.

RARJPEG

При компютърната стеганография информацията се скрива в графически или текстови файлове (т.нар. „контейнери“), чрез използването на специално програмно обезпечение. Модерни реализации на стеганографските техники най-често използват като контейнер цифрови изображения, тъй като те имат предимството, че са широко разпространени в глобалната мрежа Интернет. Дигиталните изображения могат да бъдат променени, без да се нарушат функциите им, за разлика от други видове данни, чието съдържание трябва да бъде подредено по точно определен начин, за да функционират нормално. Факт е, че човек не е способен да различи минимални разлики в цвета на едно изображение, което позволява манипулирането на информация в тези файлове. Възможни са различни начини да се скрие информация в една цифрова снимка – тя може да бъде скрита в хедърите и футърите на изображенията или просто секретните комуникационни данни да се прикачат към файла контейнер.

Подходът за скриване на данни чрез метода RARJPEG се основава на свързване на файл с изображение, така че той се състои от секция JPEG формат, последвана от секция RAR архив.Разширението на получения файл е JPEG и тазипоследователност от символи ориентира операционната система да разбере какъв вид данни се съдържа във файла и да стартира програмата, за която е предназначен този файл. Софтуерът за преглеждане на изображения ще прочете JPEG формата до границата записана в заглавната част на JPEG файла, докато инструментът за архивиране на RAR ще пренебрегне всичко преди RAR маркера за данни, който обозначава началото на архива, тъй като това може да бъде саморазархивиращ се архив SFX. Поради тези фактори е възможно изображението и архивът да се свържат в един файл, който ще придобие функционалността и на двата файлови формата. Следователно, ако такъв файл е отворен с програма за преглеждане на изображения, тя ще покаже изображението, но ако бъде отворен с архиватор RAR, той ще покаже съдържанието на RAR архива.

С метода RARJPEGможете да скриете почти всеки файл (включително .exe) в нормално цифрово изображение. При него като статични контейнери в стеганографската система се използват цифрови фотографии– най-често в графичния формат за компресиране JPEG (като най-разпространеният и популярен формат), но също и PNG, GIF и т.н.

Скритото съобщение в зависимост от алгоритъма на компресиране е архив RAR (ZIP, 7Zи множество други), в който се съдържат един или няколко файла от произволен тип с конфиденциална информация.

Контейнерът с вграденото съобщение, наречен още стегофайл при метода RARJPEGе сумарен файл, който се възприема катоJPEGформат, което позволява лесно разпространение в интернет и значително намалява вероятността от откриване на предаваната поверителна информация.

ПРИНЦИП НА ДЕЙСТВИЕ



Фиг. 1

На Фиг. 1, лявата снимка е незапълнен носещ файл – контейнер, представляващ графично неподвижно изображение във формат JPEG, а дясната снимка е полученият стегофайл след вграждане на скритото съобщение, коетое RAR архив,в който се съдържат два файла „скрито съобщение 1.png“ и „скрито съобщение 2.docx“ (конфиденциалната информация е ограничена до два файла) – Фиг. 2
