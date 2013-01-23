monjava
=======

projet java
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE struts PUBLIC
"-//Apache Software Foundation//DTD Struts Configuration 2.0//EN"
"http://struts.apache.org/dtds/struts-2.0.dtd">

<struts>
<constant name="struts.enable.DynamicMethodInvocation" value="false" />
<constant name="struts.devMode" value="false" />

<package name="com.developpez.action"  namespace="/" extends="struts-default">
   
    <!-- Action de l'action de référence -->   
    <default-action-ref name="saisir_Developpeur"/> 
    <action name="saisir_Developpeur">
      <result>/jsp/saisir_Developpeur.jsp</result>
    </action>
    
    <action name="enregistrer_Developpeur" class="com.developpez.action.DeveloppeurAction" method="enregistrer">
        <result name="success">/jsp/enregistrer_Developpeur.jsp</result>
        <result name="input">/jsp/saisir_Developpeur.jsp</result>
    </action>  
    
<action name="lister_Developpeur" class="com.developpez.action.DeveloppeurAction"
  	method="lister">
		<result name="success">/jsp/lister_Developpeur.jsp</result>
</action>

<action name="supprimer_Developpeur" class="com.developpez.action.DeveloppeurAction"
		method="supprimer">
		<result name="success">/jsp/supprimer_Developpeur.jsp</result>
</action>
     
     
</package>   
</struts>
