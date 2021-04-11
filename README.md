<h1>About project</h1>
this project is a demonstration of automatic database deployment using the example of using <strong>Ansible</strong> automation for internal configuration of servers. 

So far, there is a deployment using the siem server on the <strong>ELK stack</strong>.
<h1>How it works?</h1>

<h2>Commands</h2>
<h2>Script order</h2>
<h2>How to config for yours usage</h2>
<h2>Structure</h2>

<strong>ANSIBLE-ELASTIC</strong>
	|<br>
	|<br>
	|--- tasks (execute order):<br> 
	|	|       <br>
	|	|- <strong>main.yml</strong><br>									 
	|	|								<br>							 
	|	|							<br>								 
	|	|										<br>			 
	|	|												<br>		 
	| |- <strong>ansible-install-dep.yml</strong>========> Install gnupg, add elastic GPG key, apt-transport-https, default-jre.<br>
	| |                  						         <br>
	| |           <br>
	|	|						<br>
	|	|		<br>
	|	|- <strong>ansible-elk.yml</strong>================> Install elasticsearch, kibana, logstash.<br>
	|	| 				                 
	|	| 						                
	|	| 						                       
	|	|- <strong>ansible-elastic.yml</strong>============> (null)start and cfg elastic						                 
	|	|- <strong>ansible-kibana.yml</strong>============> (null)start and cfg kibana						                 
	|	|- <strong>ansible-logstash.yml</strong>============> (null)start anf cfg logstash					                 
	|	 						                <br> 
	|	 					  <br>
	|--- templates<br>
	|	|<br>
	|	|- <strong>jvm.options.j2</strong> =================> javamachine options<br>
	|	|<br>
	|	|- <strong>elasticsearch.yml.j2</strong> ===========> elasticsearch options<br>
	|	|<br>
	|	|- <strong>elasticsearch.repo</strong> =============> (null)<br>
	|	|<br>
	|	|- <strong>kibana.yml.j2</strong> =============> kibana options<br>
	|<br>
	|<br>
	|--- vars (variables folder)<br>
	| |<br>
	| |- <strong>elastic-cfg.yml</strong> ========> Contains main elastic configs<br>
	| |<br>
	| |- <strong>kibana-cfg.yml</strong> ========> Contains main kibana configs<br>
	| |<br>
	| |- <strong>logstash-cfg.yml</strong> ========> Contains main kibana configs<br>
	| |<br>
	| |- <strong>install-variables.yml</strong> ==> Contains variables only for installing proc<br>
