# Manual:Parametric objects/ru
<div class="mw-translate-fuzzy">





</div>


{{Manual:TOC/ru}}

FreeCAD спроектирован для параметрического моделирования. Это значит, что создаваемая Вами геометрия не свободно лепится, а производится правилами и параметрами. Например, цилиндр должен создаваться по радиусу и высоте. С этими двумя параметрами программа имеет достаточно информации для построения цилиндра.

Параметрические объекты в FreeCAD это фактически небольшие куски программ, запускаемые при изменении параметров. Объекты могут иметь множество различных типов параметров: числа (целые вроде 1, 2, 3 или действительные с плавающей точкой вроде 3.1416), реальные размеры (1mm, 2.4m, 4.5ft), координаты (x,y,z), текстовые строки (\"Привет!\") и другие.

Последний тип позволяет быстро построить сложную цепочку операций, где каждый новый объект базируется на предыдущем, и добавление к ним новых возможностей.

В примере ниже твердотельный кубический объект (Pad) базируется на плоской прямоугольной форме (Sketch) и имеет дальность вытягивания. С этими двумя параметрами он производит твёрдое тело вытягиванием базовой формы на данное расстояние. Мы можете затем использовать этот объект как базу для дальнейших операций, таких как рисование новых двумерных форм на его грани (Sketch001) и затем выреза (Pocket), вплоть до получения финального объекта.

Все промежуточные операции (двумерные формы, подкладки, выемки и так далее) остаются, и можно изменить любой из их параметров в любое время. Вся цепочка будет пересчитана при необходимости.

![](images/Parametric_objects.jpg )

Необходимо понимать две важные вещи:

1.  Рекомпиляция не всегда автоматическая. Тяжёлые операции, которые должны модифицировать большую часть вашего документа и должны занять много времени, не производятся автоматически. Вместо этого объекты (и все зависимые от них объекты) отмечаются как нуждающиеся в рекомпиляции (в древе проекта рядом с ними появляется маленькая голубая иконка). После этого Вы должны нажать кнопку рекомпиляции (или **Правка->Обновить**), чтобы перекомпилировать все отмеченные объекты.
2.  Древо зависимости должно всегда идти в том же направлении. Петли недопустимы (см. [DAG](Glossary/ru#Directed_Acyclic_Graph.md), и [DAG view](DAG_view/ru.md)). Вы можете иметь объект, зависящий от объекта Б, который зависим от объекта В, но Вы не можете иметь объект А, который зависит от объекта Б, зависимого от объекта А. Это будет круговая зависимость. Однако Вы можете иметь множество объектов зависимых от одного объекта, например, объект Б и В может зависеть от объекта А. Меню **Инструменты -> Граф зависимостей** покажет Вам диаграмму зависимостей вроде картинки выше. Это может быть полезно для определения проблем.

Не все объекты в FreeCAD параметрические. Зачастую импортируемая из других файлов геометрия не содержит параметров, и будет простой, не параметрической. Тем не менее, они обычно могут использоваться как база или стартовая точка для новых параметрических объектов, разумеется, в зависимости от их требований и качества импортируемой геометрии.

Все объекты, параметрические или нет, будут иметь множество базовых параметров, таких как Имя, уникальное в документе и не редактируемое, Метку, представляющую собой редактируемое пользовательское имя, и [размещение](placement/ru.md), устанавливающее позицию в трёхмерном пространстве.

В конце стоит отметить, что пользовательские параметрические объекты [легко программировать на python](Scripted_objects/ru.md).

**Читать далее**


<div class="mw-translate-fuzzy">

-   [Редактор параметров](Property_editor/ru.md)
-   [Как программировать параметрические объекты](Scripted_objects/ru.md)
-   [Расположение объектов в FreeCAD](Placement/ru.md)
-   [Включение графа зависимостей](Std_ExportGraphviz/ru.md)


</div>


<div class="mw-translate-fuzzy">





</div>



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Poweruser Documentation](Category_Poweruser Documentation.md) > [Tutorials](Category_Tutorials.md) > Manual:Parametric objects/ru
