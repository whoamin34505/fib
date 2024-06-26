<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <link rel="icon" href="https://i.imgur.com/HpPTBME.png">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Памятка FIB</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: "Montserrat", sans-serif;
            font-optical-sizing: auto;
            margin: 0;
            padding: 0;
        }

        table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0;
            border: 1px solid #ddd;
            border-radius: 12px;
            overflow: hidden;
            margin-top: 20px;
        }

        th,
        td {
            padding: 12px 15px;
            text-align: left;
            position: relative;
        }

        th {
            background-color: #f4f4f4;
            font-weight: bold;
        }

        th:first-child {
            border-top-left-radius: 12px;
        }

        th:last-child {
            border-top-right-radius: 12px;
        }

        td {
            background-color: #fff;
        }

        tbody tr:hover {
            background-color: #f1f1f1;
        }

        td:first-child,
        th:first-child {
            border-left: none;
        }

        td:last-child,
        th:last-child {
            border-right: none;
        }

        tbody tr:last-child td:first-child {
            border-bottom-left-radius: 12px;
        }

        tbody tr:last-child td:last-child {
            border-bottom-right-radius: 12px;
        }

        th,
        td {
            border-top: 1px solid #ddd;
            border-bottom: 1px solid #ddd;
        }

        th+th,
        td+td {
            border-left: 1px solid #ddd;
        }

        th:nth-child(1),
        td:nth-child(1),
        th:nth-child(3),
        td:nth-child(3) {
            width: 10%;
        }

        th:nth-child(2),
        td:nth-child(2) {
            width: 80%;
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: white;
            z-index: 1000;
            padding: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav h1 {
            font-size: 18px; /* Уменьшил размер шрифта для заголовка навигации */
            margin: 0;
        }

        nav ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
            display: flex;
            gap: 10px;
        }

        nav ul li {
            margin-bottom: 10px; /* Уменьшение отступа между строками */
        }

        nav ul li a {
            font-size: 14px; /* Уменьшил размер шрифта для ссылок навигации */
            text-decoration: none; /* Убираем подчеркивание */
            color: #000; /* Цвет текста */
            padding: 5px 10px;
            display: block;
            transition: background-color 0.3s ease; /* Плавное изменение фона */
        }

        nav ul li a:hover {
            background-color: #ddd; /* Цвет подсветки при наведении */
        }

        section {
            margin-top: 70px; /* Увеличил отступ для компенсации фиксированной навигации */
        }

        .highlight {
            background-color: yellow;
        }

        mark {
            background-color: yellow;
            color: black;
        }

        html {
            scroll-behavior: smooth;
        }
        .offset {
            margin-top: 4%; /* This should match the height of your nav */
        }
    </style>
</head>
<body>
    <nav>
        <h1>Навигация</h1>
        <ul>
            <li><a href="#miranda"> ● Миранда</a></li>
            <li><a href="#zalog"> ● Залог</a></li>
            <li><a href="#uk"> ● Уголовный кодекс</a></li>
        </ul>
        <input type="text" id="search" placeholder="Поиск...">
    </nav>
    <p class="offset">
    <p>
        <h2 id="miranda">Миранда</h2>
        <a>Вы имеете право хранить молчание. 
            Всё, что вы скажете,
             будет использовано против Вас в суде.
             Вы имеете право на адвоката.
             Если не сможете оплатить услуги адвоката,
             то он будет предоставлен государством. 
            Вы имеете право на один телефонный звонок, 
            длительностью не более 5 минут.
             Вы понимаете свои права?</a>
    </p>
    <p>
        <h2 id="zalog">Залог</h2>
        <a>✭ - 25к - 7 минут</a><br>
        <a>✭✭ - 50к - 14 минут</a><br>
        <a>✭✭✭ - 75к - 21 минута</a><br>
        <a>✭✭✭✭ - 100к - 28 минут</a><br>
        <a>✭✭✭✭✭ - без залога - 35 минут</a><br>
    </p>
    <h1 id="uk">Уголовный кодекс</h1>
    <table>
        <thead>
            <tr>
                <th>Статья</th>
                <th>Описание</th>
                <th>Звёзды</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>6.1</td>
                <td>Умышленное нанесение телесных повреждений.</td>
                <td>✭✭✭</td>
            </tr>
            <tr>
                <td>6.1.1</td>
                <td>Умышленное нанесение тяжких телесных повреждений, повлекшие за собой потерю сознания.</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>6.2</td>
                <td>Посягательство на жизнь человека (Попытка - 4 звезды. Два+ человека - 5 звезд + изъятие лиц. на оруж.)</td>
                <td>✭✭✭✭ или ✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>6.3</td>
                <td>Убийство (+ изъятие лиц. на оруж)</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>6.3.1</td>
                <td>Убийство с особой жестокостью (Групповое, особоопасн. путем, из корыстных целей, по найму) + изъятие лиц. на оруж</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>6.4</td>
                <td>Убийство по неосторожности</td>
                <td>✭✭✭</td>
            </tr>
            <tr>
                <td>6.6</td>
                <td>Угроза расправой над гражданским лицом, либо угроза применения насилия(оружия) в отношении его близких</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>7.1</td>
                <td>Похищение</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>7.2</td>
                <td>Клевета</td>
                <td>✭✭✭</td>
            </tr>
            <tr>
                <td>9.5</td>
                <td>Запугивание, шантаж, а так же наличие реальных оснований угрозе жизни такими действиями (Пример: оружие за спиной или в руках)</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>10.4</td>
                <td>Грабеж</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>10.5</td>
                <td> Ограбление в розыске (подробнее на форуме)</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>10.6</td>
                <td>Угонка</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>10.6.1</td>
                <td>Угон государственного имущества</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>10.8</td>
                <td>Умышленное уничтожение или повреждение государственного имущества</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>12.1</td>
                <td>Терроризм</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>12.6</td>
                <td>Незаконное нахождение на охраняемой территории</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>12.6.1</td>
                <td>Незаконное проникновение или нахождение на закрытой территории в соответствии c законом “О государственных территориях”</td>
                <td>✭✭✭</td>
            </tr>
            <tr>
                <td>12.6.2</td>
                <td>Незаконное проникновение или нахождение на объекте особой важности</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>12.7</td>
                <td>Незаконные приобретение, передача, сбыт, хранение, изготовление, перевозка, использование или ношение любых видов оружия,
                    боеприпасов, взрывчатки или иных взрывчатых веществ, а также спецсредств государственного образца</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>13.1</td>
                <td>Незаконное приобретение, хранение, перевозка, изготовление, переработка наркотических веществ или психотропных средств без цели сбыта</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>13.2</td>
                <td>Незаконное производство, сбыт или пересылка наркотических веществ, психотропных средств или их аналогов</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>15.4</td>
                <td>Злоупотребление должностными полномочиями (подробнее на форуме)</td>
                <td>"✭✭✭ или ✭✭✭✭"</td>
            </tr>
            <tr>
                <td>15.5</td>
                <td>Дача/получение взятки (подробнее на форуме)</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>15.6</td>
                <td>Халатность (подробнее на форуме)</td>
                <td>"✭✭✭ или ✭✭✭✭✭"</td>
            </tr>
            <tr>
                <td>15.7</td>
                <td>Незаконная выдача должностным лицом документа государственного образца. Незаконная выдача должностным лицом лицензии, справки или иного документа государственного образца, а равно выдача такого документа без должных на то оснований</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>16.4</td>
                <td>Привлечение заведомо невиновного к уголовной или административной ответственности</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>16.5</td>
                <td>Заведомо незаконное задержание, заключение под стражу или содержание под стражей</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>16.12</td>
                <td>Злостное неисполнение вступивших в закон. силу приг. суда, решения суда или иного судебного акта, постановления прокурора или выданного ордера а равно воспрепятствование их исполнению</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>16.15</td>
                <td>Уклонение от отбывания ограничения свободы или лишения свободы. Исключение: Лица, добровольно явившиеся для оформления явки с повинной, получают 1/2, установл. настоящей статьей, наказания</td>
                <td>от ✭ до ✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>17.1</td>
                <td>Посягательство на жизнь сотрудника государственной организации</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>17.2</td>
                <td>Угроза расправой над сотрудником государственной организации и/или угроза применения насилия или оружия</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>17.3</td>
                <td>Оскорбление сотрудника (-ов) государственной структуры, при исполнении им (-и) своих служебных обязанностей Примечание: Оскорбление - унижение чести и достоинства другого лица, выраженное в неприличной или иной противоречащей общепринятым нормам морали и нравственности форме.</td>
                <td>✭✭✭</td>
            </tr>
            <tr>
                <td>17.8</td>
                <td>Помеха работе правоохранительных органов, повлекшая за собой упущение задержанного/преследуемого/арестованного</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>17.9</td>
                <td>Провокация государственного служащего при исполнении</td>
                <td>✭✭✭</td>
            </tr>
            <tr>
                <td>17.10</td>
                <td>Попытка побега, равное побегу с места и/или во время задержания/ареста</td>
                <td>✭✭✭</td>
            </tr>
            <tr>
                <td>17.12</td>
                <td>Применение насилия в отношении сотрудника государственной структуры, находящегося при исполнении служебных обязанностей</td>
                <td>✭✭✭✭</td>
            </tr>
            <tr>
                <td>19.1</td>
                <td>Кейс-файл на рейд определенной преступной фракции (подробнее на форуме)</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>19.2</td>
                <td>Участие в преступном сообществе</td>
                <td>✭✭✭✭✭</td>
            </tr>
            <tr>
                <td>17.6</td>
                <td>Неповиновение законному требованию или приказу Примечание: При осуществлении профессиональной деятельности необходимо предъявить свое удостоверение по первому требованию. Перед требованием удостоверения необходимо предъявить свое сотруднику. Подобное действие представляет собой административное правонарушение, предусмотренное статьей 2.9 АК SA. За отказ предъявить служебное удостоверение сотруднику правоохранительного органа или госслужащему должностные лица могут быть оштрафованы на 15 000 долларов.</td>
                <td>✭✭✭✭</td>
            </tr>
        </tbody>
    </table>
    </p>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const searchInput = document.getElementById('search');
            const paragraphs = document.querySelectorAll('p, td');
            let timeoutId;

            const searchHandler = function() {
                const searchTerm = searchInput.value.trim().toLowerCase();

                if (timeoutId) {
                    clearTimeout(timeoutId);
                }

                timeoutId = setTimeout(function() {
                    console.log(`Searching for: ${searchTerm}`);

                    let firstMatchFound = false;

                    paragraphs.forEach(paragraph => {
                        const paragraphText = paragraph.textContent.toLowerCase();
                        const originalHtml = paragraph.innerHTML;

                        // Clear previous highlights
                        paragraph.innerHTML = paragraphText;

                        if (searchTerm) {
                            const searchRegex = new RegExp(`(${searchTerm.replace(/[.*+?^${}()|[\]\\]/g, '\\$&')})`, 'gi');
                            const highlightedHTML = paragraphText.replace(searchRegex, match => `<mark>${match}</mark>`);
                            paragraph.innerHTML = highlightedHTML;

                            if (!firstMatchFound && highlightedHTML !== paragraphText) {
                                // Scroll to the first match
                                paragraph.scrollIntoView({ behavior: 'smooth', block: 'center' });
                                firstMatchFound = true;
                            }
                        }
                    });

                }, 200); // Увеличил задержку до 200 мс для более комфортного ввода
            };

            // Добавляем обработчик события input для поля поиска
            searchInput.addEventListener('input', searchHandler);

            // Обработчик кликов по ссылкам в навигации
            document.querySelectorAll('nav ul li a').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();

                    const targetId = anchor.getAttribute('href').substring(1);
                    const targetElement = document.getElementById(targetId);
                    const navHeight = document.querySelector('nav').offsetHeight;

                    if (targetElement) {
                        const targetPosition = targetElement.getBoundingClientRect().top + window.pageYOffset - navHeight;
                        window.scrollTo({
                            top: targetPosition,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>
</body>
</html>
