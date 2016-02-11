## Как собрать стоп-слова самим Сфинксом

`indexer` умеет выбирать самые частые слова в индексе:

```bash
indexer --buildstops stopwords.txt 300 --config config/development.sphinx.conf your_index_core
```

В `stopwords.txt` окажутся 300 самых популярных слов, большая часть из которых — предлоги.
