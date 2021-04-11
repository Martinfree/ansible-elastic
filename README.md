
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
	|--- <strong>tasks </strong>(execute order):<br> 
	|	|       <br>
	|	|- <strong><strong>main.yml</strong></strong><br>									 
	|	|								<br>							 
	|	|							<br>								 
	|	|										<br>			 
	|	|												<br>		 
	| |- <strong>ansible-install-dep.yml</strong></strong>========> Install gnupg, add elastic GPG key, apt-transport-https, default-jre.<br>
	| |                  						         <br>
	| |           <br>
	|	|						<br>
	|	|		<br>
	|	|- <strong>ansible-elk.yml</strong></strong>================> Install elasticsearch, kibana, logstash.<br>
	|	| 				                 
	|	| 						                
	|	| 						                       
	|	|- <strong>ansible-elastic.yml</strong>============> (null)start and cfg elastic						                 
	|	|- <strong>ansible-kibana.yml</strong></strong>============> (null)start and cfg kibana						                 
	|	|- <strong>ansible-logstash.yml</strong></strong>============> (null)start anf cfg logstash					                 
	|	 						                <br> 
	|	 					  <br>
|--- <strong>templates<br></strong>
|	|<br>
|	|- <strong>jvm.options.j2</strong></strong> =================> javamachine options<br>
|	|<br>
|	|- <strong>elasticsearch.yml.j2</strong></strong> ===========> elasticsearch options<br>
|	|<br>
|	|- <strong>elasticsearch.repo</strong></strong> =============> (null)<br>
|	|<br>
|	|- <strong>kibana.yml.j2</strong> =============> kibana options<br>
|<br>
|<br>
|--- <strong>vars (variables folder)<br></strong>
| |<br>
| |- <strong>elastic-cfg.yml</strong> ========> Contains main elastic configs<br>
| |<br>
| |- <strong>kibana-cfg.yml</strong>========> Contains main kibana configs<br>
| |<br>
| |- <strong>logstash-cfg.yml </strong>========> Contains main kibana configs<br>
| |<br>
| |- <strong>install-variables.yml </strong>==> Contains variables only for installing proc<br>
