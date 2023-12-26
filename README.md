# Desription create email
## Требования к верстке писем
  <ol>
    <li>Письмо не должно превышать <b>102КБ</b>;</li>
    <li>Все стили для элементов пишутся инлайново на элементах;</li>
    <li>Дополнительные стили для классов адаптива или например, темной темы записываются в теге style;</li>
      <blockquote>
        <pre>
.class-adaptive-full {
  width: 100%;
  padding: 20px;
}
        </pre>
      </blockquote>
    <li>Медиа запросы записываются в теге style:
      <blockquote>
        <pre>
@media(max-width: 552px) {
  .class-adaptive-552px {
    width: 50%;
    padding: 10px;
  }
}
        </pre>
      </blockquote>
    </li>
    <li>Не должно быть подключения файлов: <b>js</b> или <b>css</b>;</li>
    <li>Все элементы находящиеся в строке должны оборачиваться в колонки <b>&lt;td&gt;</b>;</li>
    <li>Теги которые не имеют закрывающего тега должны закрываться. Например тег  <b>img</b>.</li>
    <li>
      Обязательно:
      <ul>
        <li>
          прописать для тега &lt;img&gt;
          <ul>
            <li>alt и title</li>
          </ul>
        </li>
      </ul>
      <ul>
        <li>
          прописать для тега &lt;a&gt;
          <ul>
            <li>role</li>
            <li>указывается target="_blank"</li>
          </ul>
        </li>
      </ul>
      <ul>
        <li>
          для каждой таблицы прописывается вид:
          &lt;table border='0' cellspacing='0' cellpadding='0' role='presentation'&gt;&lt;/table&gt;
          <ul>
            <li>role='presentation' - для корректной работы screen reader, чтобы screen reader программы могли корректно читать и поддерживать интерфейсы/li>
        </ul>
      </li>
  </ol>

  <hr>


## Основные теги:
  <ul>
    <li>table</li>
    <li>tr</li>
    <li>td</li>
    <li>thead</li>
    <li>tbody</li>
    <li>p</li>
    <li>span</li>
    <li>heading: h1 h2 h3 и тд</li>
    <li>img</li>
    <li>a</li>
  </ul>

  <hr>


## Адаптивная верстка письма
#### Инлайновость:
  <ul>
    <li>
      при верстке для адаптива можно использовать display inline, для него Обязательно нужно указывать font-size: 0; тк существуют "фантомные" отступы у инлайн элементов
    </li>
  </ul>

  <hr>

## Для OUTLOOK:
  <blockquote>
    обязательное использование конструкций фантомной таблицы:
  </blockquote>

  <blockquote>
    - "фантомная"
    <pre>
      &lt;!-- [if (gte mso 9)|(IE)] --&gt;
        &lt;table border='0' cellspacing='0' cellpadding='0' role='presentation'&gt;&lt;/table&gt;
          &lt;tr&gt;
            &lt;td&gt;
      &lt;![endif]--&gt;
    </pre>
  </blockquote>
  <blockquote>
    <контент>
  </blockquote>
  <blockquote>
    - "обычная"
    <pre>
      &lt;!-- [if (gte mso 9)|(IE)] --&gt;
          &lt;td&gt;
        &lt;tr&gt;
      &lt;/table&gt;
      &lt;![endif]--&gt
    </pre>
  </blockquote>
  <blockquote>
    фантомная таблица будет показана в Outlook, а обычная будет в других почтовиках
  </blockquote>

  <hr>

##### Правила поддерживают почтовики
  <ul>
    <li>
      Apple mail
    </li>
    <li>
      Gmail
    </li>
    <li>
      Outlook
    </li>
    <li>
      Yahoo
    </li>
    <li>
      Mail Почта
    </li>
    <li>
      Yandex Почта
    </li>
    <li>
      Sumsung mail
    </li>
  </ul>
