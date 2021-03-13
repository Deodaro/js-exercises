## Объекты

Функция, которая считает количество слов в предложении и возвращает объект. Свойства этого объекта -- слова, значения -- то, сколько раз это слово встретилось в предложении. Перед подсчётом слова преобразуются в нижний регистр, чтобы избежать дублей.

```js
import _ from 'lodash';

const countWords = (str) => {
  const words = _.words(str.toLowerCase());
  const result = {};
  for (const word of words) {
    if (_.has(result, word)) {
      result[word] += 1;
    } else {
      result[word] = 1;
    }
  }

  return result;
};
```

