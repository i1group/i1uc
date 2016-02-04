# i1uc
An English version of this text is contained below.

Модуль синхронизации атрибутов продукта с полями ноды типа "ссылка на термин"

Знакома ситуация, когда нужно дублировать атрибуты каждого товара в термины таксономии (т.е. соответствующие поля ноды)? Этот модуль позволяет решить эту задачу.

ФУНКЦИИ
+ Автоматическое копирование (синхронизация) атрибутов в поле ноды (термины таксономии) при сохранении атрибутов на странице редактирования параметров товара (типа node/123/edit/options).
+ Массовая синхронизация атрибутов для всех товаров.

ПОДРАЗУМЕВАЕТСЯ, ЧТО У ВАС
+ Есть магазин на drupal7 + ubercart3.
+ Созданы атрибуты продука (admin/store/products/attributes) и соответствующие словари таксономии (admin/structure/taxonomy).
+ Термины в этих словарях и опции в этих атрибутах уже созданы и имеют одинаковые имена.
+ Есть тип материала для продукта, в котором созданы поля типа "ссылка на термин", указывающие на вышеупомянутые словари.

ЧТОБЫ ЗАРАБОТАЛО
+ Откройте файл i1uc.module и замените значения переменных своими данными: строки 13-27.
+ Включите модуль в админке друпала.
Всё. Теперь каждый раз, когда пользователь будет редактировать атрибуты товара, они автоматически будут копироваться в соответствующие поля.

МАССОВАЯ СИНХРОНИЗАЦИЯ
Если нужна массовая синхронизация атрибутов для уже созданных продуктов, просто откройте страницу:
http://mysite.net/make_ubercart_product_attributes_happy

Здесь также можно ограничивать количество обрабатываемых продуктов через параметры:
http://mysite.net/make_ubercart_product_attributes_happy?start=1000&limit=300

Наслаждайтесь!
Создано студией i1group.ru


****

Module for product attributes to node fields (of "term reference" type) synchronization

Are you familiar with situation, when it is required to copy all product attributes to taxonomy terms (e.g corresponding node fields)? This module can handle this.

FUNCTIONS
+ Automatic copying (synchronization) of product attributes to product node fields (taxonomy terms), when saving attributes on product parameters page (like node/123/edit/options).
+ Batch synchronization of attributes for all products.

IT MEANS THAT YOU HAVE:
+ A shop build with drupal7 + ubercart3.
+ You've already created product attributes (admin/store/products/attributes) and corresponding taxonomy vocabularies (admin/structure/taxonomy).
+ Terms in these vocabularies and options in these attributes are already created and have same names.
+ You have node type for the product, and fields of "term reference" type are created pointing to mentioned vocabularies.

HO TO MAKE IT WORK
+ Open i1uc.module file and replace variable values with your data: lines 13-27.
+ Enable module in drupal admin section.

Thats it. Now every time, when user edits attributes of a particular product they will be automatically copied to corresponding fields.

BATCH SYNCHRONIZATION
If you need batch synchronization of attributes for all products of your site, just open this page:
http://mysite.net/make_ubercart_product_attributes_happy

You can also limit quantity of processed products via parameters:
http://mysite.net/make_ubercart_product_attributes_happy?start=1000&limit=300

Enjoy!
Developed by i1group.ru
