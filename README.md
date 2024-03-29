<h1>fadeBlock - плагин анимированного появление блоков</h1>
<img src="https://www.denyspopov.com/wp-content/themes/denyspopov/image/fade.gif" width="100%">


Автор плагина: <a href="https://www.denyspopov.com">Denys Popov</a>

При помощи данного плагина можно реализовать анимированное появление и исчезновение блоков при скролле сайта

Плагин написан на чистом JS
<h2>Особенностей плагина fadeBlock</h2>
<ul>
  <li>определяет,находится ли нужный блок в области просмотра, и затем добавляет класс к нему;</li>
  <li>5 встроенных анимаций;</li>
  <li>можно настроить скорость анимации;</li>
  <li>настройка отступа от низа экрана браузера для анимированного появления блока;</li>
  <li>можно включить исчезновение блоков, если скролить сайт на верхпростая настройка.</li>
</ul>

<h2>Как им пользоваться</h2>

1. На блоки которые должны появлятся при скролле страницы необходимо развесить классы:

<b>fadeIn</b> - появление блока без смещений <br>
<b>fadeRight</b> - появление блока справа <br>
<b>fadeLeft</b> - появление блока слева <br>
<b>fadeTop</b> - появление блока сверху <br>
<b>fadeBottom</b> - появление блока снизу <br>

2. Подключение js плагина.
-js можно подключить в шапке или футере сайта.
-Желательно подключить его перед вашими основными скриптами
-после подключения скрипта вам необходимо задать настройки появления

3. Что бы задать настройки для плагина, вам необходимо после подключенной js плагина, вставить строку с настройкой, которая выглядит след. образом:
<pre>
  <code>
    <script>
      const fadeOptions = new Options(animationTime, pixelsFromBottom, reverseFade);
    </script>
  </code>
</pre>
либо можно прописать в самом конце js-файла плагина fadeBlock.js строку с настройками
<pre>
  <code>
      const fadeOptions = new Options(animationTime, pixelsFromBottom, reverseFade);
  </code>
</pre>
<table>
  <tr>
    <th>
      Параметры
    </th>
    <th>
      Описание
    </th>
    <th>
      Значение
    </th>
    <th>
      default
    </th>
  </tr>
  <tr>
    <td>
      <b>animationTime</b>
    </td>
    <td>
      Время анимации
    </td>
    <td>
      1,2, 2.5,3 и т.д
    </td>
    <td>
      1
    </td>
  </tr>
    <tr>
    <td>
      <b>pixelsFromBottom</b>
    </td>
    <td>
      Отступ от низа экрана браузера
    </td>
    <td>
      50, 100, 124 и т.д
    </td>
    <td>
      0
    </td>
  </tr>
    </tr>
    <tr>
    <td>
      <b>reverseFade</b>
    </td>
    <td>
       Исчезновение блоков, если проскролить сайт обратно вверх
    </td>
    <td>
      true / false
    </td>
    <td>
      false
    </td>
  </tr>
</table>
Расшифровка на реальном примере:
<code>const fadeOptions = new Options(1, 100, false);</code><br>
<pre>
-Время анимации 1 секунда
-Появление блока будет происходить когда он будет находится на расстоянии 100 пикселей от низа экрана
-При скролле вверх блоки исчезать не будут
</pre>

Если есть вопросы или предложения по работе плагина, пишите на почту popovdenys@gmail.com
