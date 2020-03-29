# Development Environment

- ## The maven global path configuration failure when IDEA restart

``` xml
1. Env: win10,idea2019.2
2. Edit file "project.default.xml" in C:\Users\Lenovo\.IntelliJIdea2019.2\config\options .

<application>
	<component name="ProjectManager">
	<defaultProject>
	  <component name="PropertiesComponent">
		<property name="settings.editor.selected.configurable" value="MavenSettings" />
	  </component>
	</defaultProject>
	</component>
  
	<!-- new component start-->
	<component name="MavenImportPreferences">
	　 <option name="generalSettings">
		  <MavenGeneralSettings>
			  <option name="localRepository" value="D:\ProgramFiles\apache-maven-3.6.3\repository" />
			  <option name="mavenHome" value="D:\ProgramFiles\apache-maven-3.6.3" />
			  <option name="userSettingsFile" value="D:\ProgramFiles\apache-maven-3.6.3\conf\settings.xml" />
		  </MavenGeneralSettings>
	　　</option>
	</component>
	<!-- new component end -->
</application>

3. Restart idea, Then open "File-Other Settings-Settings for New Project" to confirm whether it is effective.
```

