# Q&A
- Module 1
```	
	Logstash provides interface for cath->parse->filter and upgrade logs. 
	Logstash have strong instruments for create "more readable" logs format tagging
and journaling.
```
- Module 2

1. В якому файлі налаштовуються параметри -Xmx та -Xss? Для чого? Якій рекомендований розмір?
```
jvm.options settings file. For setup logstash java machine heap size.
Recommended heap size no less 4Gb
```
2. Для чого предназначений файл pipeline.yml? 
```
pipeline.yml file assign pipelines(in this case task with config) wich isolated
from other with specified config, workers.
```
3. За що відповідає параметр path.config?
```
path.config param specified path to config(s)
```
4. Для чого предназначений файл logstash.yml?
```
logstash.yml contain logstash modules, nodes, pipelines, 
workers and logstash behavior
```

- Module 3

1. Опишіть три основних структурних елемента для роботи logstash в якості 
обробника логів
```

input {...} - An input plugin enables a specific source of events to be read by Logstash.
```
```
filter {...} - A filter plugin performs intermediary processing on an event. 
Filters are often applied conditionally depending on the characteristics of the event.
```
```
output {...} - An output plugin sends event data to a particular destination. 
Outputs are the final stage in the event pipeline.
```
2. Для чого потрібно використовувати плагіни?
```
Plugins in logstash - packages wich contains ready interface for working with 
special service logs
```



