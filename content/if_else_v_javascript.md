+++
date = '2024-03-25T18:53:24+03:00'
title = 'if / else в JavaScript'
categories = [ "javascript" ]
+++

<p>Лекция про условные операторы в Udemy</p>
            <p>
              Конструкции условий дают возможность изменить ход работы программы в зависимости от
              условий, которые проверяются. Благодаря им мы можем создавать сложные программы,
              которые будут вести себя по-разному в различных сценариях.
            </p>
            <h3>if</h3>
            <p>
              Давайте создадим пример функции, которая определяет тип предложения, переданного в
              качестве аргумента. Изначально она будет различать обычные предложения от
              вопросительных.
            </p>
            <pre><code>const getTypeOfSentence = (sentence) => {
const lastChar = sentence[sentence.length - 1];
if (lastChar === '?') {
  return 'question';
}
return 'general';
};
getTypeOfSentence('Hodor');  // general
getTypeOfSentence('Hodor?'); // question</code></pre>
            <p>
              "if" - это конструкция в языке программирования, которая контролирует
              последовательность выполнения операций. Внутри скобок передается выражение-предикат,
              за которым следует блок кода в фигурных скобках. Этот блок кода выполняется только в
              случае если предикат равен true.
            </p>
            <p>
              Если предикат возвращает false, то программа пропускает блок кода в фигурных скобках и
              продолжает выполнение. В данном примере выполнится следующая строка кода: return
              'general'; - она заставит функцию вернуть строку и завершить работу. Можно заметить,
              что оператор return может быть использован в любом месте функции, включая блок кода с
              условием.
            </p>
            <p>
              Если после оператора if идет только одна строка кода в фигурных скобках, их можно
              опустить, например:
            </p>
            <pre><code>const getTypeOfSentence = (sentence) => {
const lastChar = sentence[sentence.length - 1];
if (lastChar === '?')
  return 'question';
return 'general';
}; 
console.log(getTypeOfSentence('Hodor'));  // => general
console.log(getTypeOfSentence('Hodor?')); // => question</code></pre>
            <p>
              Рекомендуется всегда использовать фигурные скобки, даже если внутри них только одна
              строка кода. Таким образом будет явно видно границы тела условия, что делает код более
              структурированным и понятным.
            </p>
            <h3>else</h3>
            <p>
              Давайте создадим функцию getTypeOfSentence(), которая анализирует текст и возвращает
              описание его тона: для декларативных предложений – General sentence, для
              вопросительных – Question sentence.
            </p>
            <pre><code>getTypeOfSentence('Hodor');  // General sentence
getTypeOfSentence('Hodor?'); // Question sentence</code></pre>
            <p>Сама функция будет такой:</p>
            <pre><code>const getTypeOfSentence = (sentence) => {
// Объявляем переменную, в которую запишем тип предложения
let sentenceType;
// Предикат, проверяющий окончание текста
// Если он оканчивается на символ '?', то вернется true,
// иначе false
if (sentence.endsWith('?')) {
  // Если условие выше сработало,
  // то это вопросительное предложение.
  // Присваиваем sentenceType соответствующее значение.
  sentenceType = 'Question';
} else {
  // Во всех остальных случаях предложение — обычное
  sentenceType = 'General';
}
// С помощью интерполяции формируем строку
return `${sentenceType} sentence`;
};</code></pre>
            <p>
              Мы внесли изменения, добавив ключевое слово "else" и новый блок с фигурными скобками.
              Этот блок будет выполнен только в случае, если условие в выражении "if" будет
              возвращать false.
            </p>
            <h3>Конструкция else if</h3>
            <p>
              Функция getTypeOfSentence() в предыдущем примере определяет только вопросительные и
              обычные предложения. Давайте попробуем расширить функциональность, чтобы она также
              поддерживала восклицательные предложения.
            </p>
            <pre><code>const getTypeOfSentence = (sentence) => {
const lastChar = sentence[sentence.length - 1];
let sentenceType; 
if (lastChar === '!') {
  sentenceType = 'exclamation';
} else {
  sentenceType = 'normal';
} 
if (lastChar === '?') {
  sentenceType = 'question';
}
return `Sentence is ${sentenceType}`;
};
getTypeOfSentence('Who?'); // Sentence is question
getTypeOfSentence('No');   // Sentence is normal
getTypeOfSentence('No!');  // Sentence is exclamation</code></pre>
            <p>
              Мы добавили дополнительную проверку на "восклицание" ("exclamation" переводится как
              «восклицание»). Технически функция работает, однако с точки зрения семантики возникают
              некоторые проблемы:
            </p>
            <p>
              1) Проверка наличия вопросительного знака выполняется в любом случае, даже если уже
              обнаружен восклицательный знак.
            </p>
            <p>2) Второе условие не учитывается в ветке else.</p>
            <p>
              Было бы правильнее воспользоваться еще одним условием для более точной работы функции.
            </p>
            <pre><code>const getTypeOfSentence = (sentence) => {
const lastChar = sentence[sentence.length - 1];
let sentenceType;
if (lastChar === '?') {
  sentenceType = 'question';
} else if (lastChar === '!') {
  sentenceType = 'exclamation';
} else {
  sentenceType = 'normal';
}
return 'Sentence is ${sentenceType}';
};
getTypeOfSentence('Who?'); // Sentence is question
getTypeOfSentence('No');   // Sentence is normal
getTypeOfSentence('No!');  // Sentence is exclamation</code></pre>
            <p>
              Теперь все условия объединены в одну конструкцию. Ветвь else if означает «если
              предыдущее условие не выполнено, но текущее выполнено».
            </p>
            <p>
              Логика выполнения будет ограничена одним из блоков кода, соответствующих всей
              конструкции if.
            </p>