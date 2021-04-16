# Q&A
- Module 1

1. Для чого призначений filebeat? В яких ситуаціях ви будете його приміняти?
```
Filebeat - agent assigned for forwarding and centralizing log data, wich monitors 
the log files or locations that you specify, collects log events
```
2. Для чого призначений metricbeat? В яких ситуаціях ви будете його приміняти?
```
Metricbeat - agent for collect metrics from the operating system and from 
services running on the server. 
```
3.  Для чого призначений auditbeat? В яких ситуаціях ви будете його приміняти?
```
Auditbeat - agent for communicating directly with the Linux audit framework, 
collects the same data as auditd
```
4.  Для чого призначений packetbeat? В яких ситуаціях ви будете його приміняти?
```
Packetbeat monitor Network protocols like HTTP, application latency, errors, 
response times, SLA performance, user access patterns and trends, and more.  
```
5. Для чого призначений winlogbeat? В яких ситуаціях ви будете його приміняти?
```
Winlogbeat works with windows logs channels.
```
6. Для чого призначений heartbeat? В яких ситуаціях ви будете його приміняти?
```
Heartbeat check the status of your services and determine whether they are available.
```
- Module 2

1. Які модулі ви обрали? Поясність свій вибір.

[Nginx module](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-module-nginx.html) - for monitor nginx logs.

[System module](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-module-system.html) - monitor sys logs.

[Iptables module](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-module-iptables.html) -parses logs received over the network via syslog or from a file.


2. Які труднощі з конфігуруванням filebeat та розумінням його ролі в вас виникли?

```
Filebeat default config - stat filebeat.yml: no such file or directory

```

- Module 3

 Сконфігурувати  input частину logstash для прийому подій filebeat

```
input { 
		beats {
			port => 5000
		}
}  
```

Сконфігурувати output частину logstash для відправки подій filebeat в elastic

```
output { 
	elasticsearch {
		hosts => ["http://localhost:9200"]
		index => "test-%{+YYYY.MM.ww}"
	}
}  
```


