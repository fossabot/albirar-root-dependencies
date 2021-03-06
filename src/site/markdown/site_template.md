# Site template

Can copy and paste this site template, and personalize:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/DECORATION/1.8.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/DECORATION/1.8.0 http://maven.apache.org/xsd/decoration-1.8.0.xsd"
	name="${name}">
	<publishDate position="left" format="dd-MM-yyy" />
	<version position="left" />
	
	<bannerLeft>
		<href>/</href>
		<title>${name}</title>
		<name>${name}</name>
	</bannerLeft>
	
	<poweredBy>
		<logo name="Albirar" title="Albirar" alt="Albirar" href="https://albirar.cat" img="images/logo-albirar-icon.png" />
	</poweredBy>
	
	<skin>
		<groupId>org.apache.maven.skins</groupId>
		<artifactId>maven-fluido-skin</artifactId>
		<version>1.9</version>
	</skin>

	<custom>
		<fluidoSkin>
			<topBarEnabled>true</topBarEnabled>
			<sideBarEnabled>false</sideBarEnabled>
		</fluidoSkin>
	</custom>


	<body>
		<head>
			<![CDATA[<link rel="icon" type="image/png" href="images/logo-albirar-icon.png"></link>]]>
		</head>
		<menu name="Documentation" title="Documentation">
			<item name="Add to your project" href="dependency.html" />
			<item name="Usage" href="usage.html" />
			<item name="Github" href="${scm.url}"  />
		</menu>
		<menu name="Info and Reports" title="Info and Reports">
			<item name="Info" href="project-info.html" />
			<item name="Reports" href="project-reports.html" />
			<item name="JavaDocs" href="apidocs" />
		</menu>
		<menu name="Code" title="Code">
			<item name="Source code" href="${scm.url}"
				title="${scm.system}"
				img="images/GitHub-Mark-32px.png">
				<description>${scm.system}</description>
			</item>
			<item name="CI" href="${ciManagement.url}"
				title="${ciManagement.system}"
				img="images/TravisCI-32px.png">
				<description>${ciManagement.system}</description>
			</item>
			<item name="Issues" href="${issueManagement.url}"
				title="${issueManagement.system} Issues"
				img="images/Octocat-32px.png">
				<description>${issueManagement.system} Issues</description>
			</item>
		</menu>
		<menu name="Releases" title="Releases">
			<item name="Maven Central" title="Maven Central"
				img="images/maven-logo-black-on-white-32px.png"
				href="https://search.maven.org/artifact/${groupId}/${artifactId}" />
		</menu>
	</body>
</project>
```