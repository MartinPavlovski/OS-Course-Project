The Senate Bus Problem
=============

Опис на проблемот
=============
<p align="center">
Овој проблем е оригинално базиран на проблемот со автобусите на колеџот Wellesley.
Патниците пристигнуваат на автобуска станица и чекаат автобус. Кога даден автобус ќе пристигне на автобуската станица сите патници кои моментално чекаат на станицата пробуваат да се качат во автобусот, но секој патник кој ќе пристигне по пристигнувањето на автобусот ќе мора да го чека следниот автобус.
Капацитетот на секој од автобусите е 50 лица. Ако на автобуската станица чекаат повеќе од 50 патници, некои од нив ќе мора да го чекаат наредниот автобус за да се качат. Кога сите предвидени патници за тековниот автобус ќе се качат во истиот, тој си заминува од автобуската станица. Ако даден автобус пристигне во момент кога на автобуската станица не чека ниту еден патник, во тој случај автобусот треба веднаш да си замине.
</p>

Протребно е да се напише програмски код за синхронизација на горенаведените настани притоа обрнувајќи внимание на следните ограничувања:

Ограничувањa
=============
- Не е дозволено повеќе од 50 патници да се качат во еден автобус.<br/>
- Не е дозволено повеќе од еден автобус да стои на автобуската станица во даден момент.<br/>
- Даден автобус не смее да ја напушти автобуската станица доколку во него не се качени сите патници(не повеќе од 50) кои првично биле на станицата кога тој пристигнал.<br/>
- Во даден автобус не е дозволено да влегуваат патници кои пристигнале на автобуската станица во момент кога тој веќе бил пристигнат на неа.<br/>
- Даден автобус не смее да стои на автобуската станица доколку при неготово пристигнување на неа немало ниту еден патник. Во ваквиот случај автобусот треба веднаш да си замине.<br/>
- Автобусот треба да ги повукува методите busArrives() и busDeparts().<br/>
- Патниците е потребно да ги повикуваат методите riderArrives() и riderBoardsBus().<br/>

Опис на методите
=============
Автобусот ги повикува методите:<br/>
- <strong>state.busArrives()</strong> – метода со која даден автобус пристигнува на автобуската станица<br/>
- <strong>state.busDeparts()</strong> – метода со која даден автобус си заминува од автобуската станица (оваа метода неможе да биде повикана доколку претходно не е повикана методата state.busArrives())<br/>

Патникот ги повикува методите:<br/>
- <strong>state.riderArrives()</strong> – метода со која еден патник пристигнува на автобуската станица<br/>
- <strong>state.riderBoardsBus()</strong> – метода со која даден патник, кој тековно чека на автобуската станица, се качува во автобусот кој се наоѓа на истата (оваа метода неможе да биде повикана доколку претходно не е повикана методата state.riderArrives() за дадениот патник и state.busArrives() за соодветниот автобус)<br/>
