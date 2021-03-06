# 5.4 Другие подходы к обучению манипулятора/клешни робота

Управления манипулятором/клешнёй робота через машинное обучение действительно только начинается. Есть несколько направлений исследований, которые я хотел бы предложить вашему вниманию, когда вы будете искать дальнейшие исследования. Одним из способов приближения к нашему пониманию движения роботов является рассмотрение баланса между эксплуатацией и разведкой. Эксплуатация - это как можно быстрее привести робота к цели. Исследование использует пространство вокруг робота, чтобы попробовать что-то новое. Программа планирования путей, возможно, застряла на локальном минимуме, и есть лучшие решения, которые не были рассмотрены.

Есть также не один способ научить робота. В нашем обучении мы использовали своего рода самопознание. Что, если бы мы могли показать роботу, что делать, и заставить его учиться на примере? Мы могли бы позволить роботу наблюдать за человеком, выполняющим ту же задачу, и заставить его попытаться подражать результатам.

## Google’s SAC-X

Google пытается немного по-другому подойти к проблеме манипулятора/клешни робота.  В своей программе SACX, которая расшифровывается как "Плановое вспомогательное управление"- Scheduled Auxiliary Control, они предполагают, что может быть довольно сложно присвоить наградные очки отдельным движениям манипулятора/клешни робота.  Они разбивают сложную задачу на более мелкие вспомогательные задачи и дают очки за выполнение вспомогательных задач, чтобы робот мог справиться со сложной задачей. Если бы мы складывали блоки манипулятором/клешнёй робота, мы могли бы раздельно подбирать блок как одно задание, двигаться с блоком, и так далее.  Google назвал это "редкой наградой"- "sparse reward" проблема, если они делали только армирование на главной задаче, укладывая блок поверх другого.  В процессе обучения робота складывать блоки можно представить, что будут тысячи неудачных попыток, прежде чем успешный ход приведет к награде.

## Amazon Robotics Challenge

На Амазоне много чего есть.  Миллионы и миллионы коробок, деталей, кусочков и вещей заполняют их полки.   Они хотят доставить вещи с полок в маленькие коробочки, чтобы они могли отправить их вам как можно быстрее, когда вы их заказываете.  Последние несколько лет Amazon является спонсором Amazon Robotics Challenge, где они приглашали команды из университетов использовать роботов, чтобы забрать предметы с полки, и, как вы догадались, положить их в коробку. Когда вы считаете, что Amazon продает почти все, что только можно вообразить, это настоящий вызов.  В 2017 году команда из Квинсленда, Австралия, выиграла соревнование c действительно хорошей ручной системой слежения.

