# Проектная работа 2 Майснера Вильгельма  
## Описание проекта. Функциональность. Используемые технологии.  
Проектная работа 2 представляет из себя одностраничный сайт, написанный на HTML и CSS, состоящий из 12 блоков. Каждый блок несет инофрмативный характер о:
 + различных методиках обучения; 
 + трудностях, возникающих на пути к новым знаниям; 
 + историям людей об их освоении новой информации;
 + полезных ресурсах.

Практически весь сайт создан с использованием `flex` и `flex-wrap`

```CSS
.table {
  width: 1100px;
  margin-top: 0;
  margin: auto;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
```
Для некоторых элементов, например логотипов и геометрических фигур, используется свойство `position`

```CSS 
.logo_place_header {
  position: absolute;
  top: 30px;
  left: 64px;
}
```
Cсылки, при наведении на них, плавно становяться немного прозрачными

```CSS
.header__link {
  text-decoration: none;
  color: #2F80ED;
  transition: all 0.3s ease;
  opacity: 1;
}

.header__link:hover {
  opacity: 0.5;
}
```

Для осуществления поворота геометрических фигур на 360 градусов была создана отдельная анимация `@keyframes rotation`

```CSS 
@keyframes rotation {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}
```
## Планы по доработке проекта

1. В блоке [header](blocks/header) [главное изображение](blocks/header/__main-illustration/header__main-illustration.css) перекрывает [квадрат](blocks/header/__square-pic/header__square-pic.css) таким образом, что область наведения на [квадрат](blocks/header/__square-pic/header__square-pic.css) остается только в верхней его части. ![To_fix](To_fix\To_fix1.png)
Необходимо сделать область наведения по всей площади [квадрата](blocks/header/__square-pic/header__square-pic.css).   
2. Также необходимо сделать плавное возращение в исходное состояние [квадрата](blocks/header/__square-pic/header__square-pic.css) и [треугольника](blocks/kaufman/__triangle/kaufman__triangle.css) при отведении курсора в сторону (из области `:hover`).
