# Release notes 0.12/ru
Это краткое изложение наиболее интересных изменений произошедших в последней версии FreeCAD. Для получения подробной списка изменений смотри [сюда](http://www.freecadweb.org/tracker/changelog_page.php).

Предыдущие версии: [0.11](Release_notes_0.11.md)

### Стартовая страница 

-   При открытии FreeCAD в первый раз, вас приветствует страница нового стартового центра, который собирает наиболее распространенные действия, которые вы хотели бы выполнять, такие как открытие определенного инструментария, загрузка одного из последних файлов над которым вы работали, чтение последних новостей о ходе разработке FreeCAD, или посмотреть одно из множества новых видео пособий созданных героическим сообществом FreeCAD.

![](images/FreeCAD_start_center.jpg )

### Sketcher & PartDesign 

<img alt="" src=images/Rim_bling.png  style="width:800px;">

-   [Инструментарий эскизов](Sketcher_Workbench.md) подвергся серьезным изменениям по сравнению с предыдущей версией, и теперь он основывается на новом решателе ограничений, написанном для этой задачи с нуля . Инструментарий эскизов теперь может выполнять практически все операции 2D черчения [Чертежного модуля](Draft_Workbench.md) и обладает широким спектром ограничений для элементов эскиза.

-   В дополнении в [PartDesign Workbench](PartDesign_Workbench.md) тоже многое поменялось и он предлагает несколько простых (и полностью параметрических) инструментов для работы поверх эскизов, таких как экструзия, лофтинг(lofting) или revolution.

### Architecture

-   Новый [Архитектурный модуль](Arch_Workbench/ru.md) теперь является частью FreeCAD. Он все ещё на ранней стадии развития, но уже сейчас обладает парочкой удобных объектов , таких как стены и структурные элементы (колонны и балки). Они могут быть построены по существующей 2D геометрии, такой как линии, ломаные(wire) и эскизы, указав ширину и высоту, или, в случае структурных элементов, по их сечению. Они также основаны на твердых телах, и даже могут включать другие твердые тела, в качестве дополнений или даже вычетов, что позволяет использовать любую возможную геометрию.

![](images/Arch_screenshot.jpg )

-   Архитектурный модуль также обладает возможность импорта из [IFC](http://en.wikipedia.org/wiki/Industry_Foundation_Classes) , экспорта и импорта из [DAE (collada)](http://en.wikipedia.org/wiki/Collada), и специального экспортера в [OBJ](http://en.wikipedia.org/wiki/Wavefront_.obj_file) который больше подходит для архитектурных моделей, чем стандартный тип файлов.

-   В Архитектурный модуль также включена растущая коллекция инструментов упрощающих работу с Mesh(полигональными) объектами из других приложений таких как [Blender](http://www.blender.org) . Mesh объекты, если они хорошо смоделированы, могут быть легко и автоматически превращены в чистые формы, и затем в параметрические Arch объекты.

### Черчение

![](images/Draft_taskview.jpg )

-   Освободите ваше рабочее место! Draft модуль теперь обладает новым графическим интерфейсом который использует панель системных задач FreeCAD, которая собирает все информацию о взаимодействии с пользователем в одном месте, освобождено драгоценное пространство съедаемое панелью инструментов Draft.

-   Чертежные инструменты Отсечь/Удлинить(Trim/Extend) теперь могут вытягивать одну грань существующего объекта.

-   Добавлено несколько режимов привязки, позволяющие привязку к параллельной и перпендикулярной существующей линии, а также к местам которые согласуются с другими отрезками.

-   Чертежный модуль теперь обладает инструментом который создает, внутри того же документа, проекции(2D вид) любой 3D формы.

-   Чертежный объект теперь может быть создан прямо на существующей грани. Если вы не указали рабочую плоскость, то она будет временно адаптирована к лежащей под ней гранью.

-   Теперь чертежный модуль может импортировать кривые Безье из SVG файлов.


{{languages | {{en|Release_notes_0.12}} {{es|Release_notes_0.12/es}} {{fr|Release_notes_0.12/fr}} {{it|Release_notes_0.12/it}} {{pl|Release_notes_0.12/pl}} }}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [News](Category_News.md) > [Documentation](Category_Documentation.md) > [Releases](Category_Releases.md) > Release notes 0.12/ru
