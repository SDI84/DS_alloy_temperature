
# DS_alloy_temperature

## Задача: 
Построение модели предсказания температуры стали. 
### Описание этапа обработки:
Сталь обрабатывают в металлическом ковше вместимостью около 100 тонн. Чтобы ковш выдерживал высокие температуры, изнутри его облицовывают огнеупорным кирпичом. Расплавленную сталь заливают в ковш и подогревают до нужной температуры графитовыми электродами. Они установлены в крышке ковша.   
Из сплава выводится сера (десульфурация), добавлением примесей корректируется химический состав и отбираются пробы. Сталь легируют — изменяют её состав — подавая куски сплава из бункера для сыпучих материалов или проволоку через специальный трайб-аппарат (англ. tribe, «масса»).  
Перед тем как первый раз ввести легирующие добавки, измеряют температуру стали и производят её химический анализ. Потом температуру на несколько минут повышают, добавляют легирующие материалы и продувают сплав инертным газом. Затем его перемешивают и снова проводят измерения. Такой цикл повторяется до достижения целевого химического состава и оптимальной температуры плавки.  
Тогда расплавленная сталь отправляется на доводку металла или поступает в машину непрерывной разливки. Оттуда готовый продукт выходит в виде заготовок-слябов (англ. slab, «плита»).  
### Описание данных:
Данные состоят из файлов, полученных из разных источников:  
- data_arc_new.csv — данные об электродах;  
- data_bulk_new.csv — данные о подаче сыпучих материалов (объём);  
- data_bulk_time_new.csv — данные о подаче сыпучих материалов (время);  
- data_gas_new.csv — данные о продувке сплава газом;  
- data_temp_new.csv — результаты измерения температуры;  
- data_wire_new.csv — данные о проволочных материалах (объём);  
- data_wire_time_new.csv — данные о проволочных материалах (время).  
Во всех файлах столбец key содержит номер партии. 
В файлах может быть несколько строк с одинаковым значением key: они соответствуют разным итерациям обработки.

## Используемые библиотеки:
	
	pandas –  для анализа и обработки данныйх; 
	sklearn – библиотека машинного обучения;
	catbost, lightgbm – библиотеки машинного обучения использующие метод градиентного бустинга;
	optuna – фреймворк для поиска оптимальных гиперпараметров моделей; 
	shap –анализ важности факторов построенной модели;
	mathplotlib, seaborn – для построения графиков,тепловых карт;
	os – модуль для работы с операционной системой;
	re – для работы с регулярными выражениями. 

## Файлы:
DS_alloy_temperature.ipynb - файл Jupyter Notebook содержащий описание обработки данных и реализации модели предсказания температуры.