
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
	|--- <span fill="green">tasks </span>(execute order):<br> 
	|	|       <br>
	|	|- <span fill="green"><strong>main.yml</strong></span><br>									 
	|	|								<br>							 
	|	|							<br>								 
	|	|										<br>			 
	|	|												<br>		 
	| |- <span fill="green">ansible-install-dep.yml</strong></span>========> Install gnupg, add elastic GPG key, apt-transport-https, default-jre.<br>
	| |                  						         <br>
	| |           <br>
	|	|						<br>
	|	|		<br>
	|	|- <span fill="green">ansible-elk.yml</strong></span>================> Install elasticsearch, kibana, logstash.<br>
	|	| 				                 
	|	| 						                
	|	| 						                       
	|	|- <span fill="green">ansible-elastic.yml</span>============> (null)start and cfg elastic						                 
	|	|- <span fill="green">ansible-kibana.yml</strong></span>============> (null)start and cfg kibana						                 
	|	|- <span fill="green">ansible-logstash.yml</strong></span>============> (null)start anf cfg logstash					                 
	|	 						                <br> 
	|	 					  <br>
	|--- <span fill="#F4A460">templates<br></span>
	|	|<br>
	|	|- <strong>jvm.options.j2</strong></span> =================> javamachine options<br>
	|	|<br>
	|	|- <strong>elasticsearch.yml.j2</strong></span> ===========> elasticsearch options<br>
	|	|<br>
	|	|- <strong>elasticsearch.repo</strong></span> =============> (null)<br>
	|	|<br>
	|	|- <strong>kibana.yml.j2</strong> =============> kibana options<br>
	|<br>
	|<br>
	|--- <span fill="blue">vars (variables folder)<br></span>
	| |<br>
	| |- <span fill="blue">elastic-cfg.yml</span> ========> Contains main elastic configs<br>
	| |<br>
	| |- <span fill="blue">kibana-cfg.yml</span>========> Contains main kibana configs<br>
	| |<br>
	| |- <span fill="blue">logstash-cfg.yml </span>========> Contains main kibana configs<br>
	| |<br>
	| |- <span fill="blue">install-variables.yml </span>==> Contains variables only for installing proc<br>
