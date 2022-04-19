# Basiswissen GeoServer

Der [GeoServer](http://geoserver.org/) ist ein offener, Java-basierter Server,
der es ermöglicht Geodaten auf Basis der Standards des [Open Geospatial Consortium (OGC)](https://www.opengeospatial.org/)
(insb. WMS und WFS) anzuzeigen und zu editieren. Eine besondere Stärke des GeoServers
ist die Flexibilität, mit der er sich um zusätzliche Funktionalität erweitern lässt.

GeoServer ist gut dokumentiert. Die Dokumentation unterteilt sich dabei
in eine Benutzer- und eine Entwicklerdokumentation:

* Benutzerdokumentation: [https://docs.geoserver.org/stable/en/user/](https://docs.geoserver.org/stable/en/user/)
* Entwicklerdokumentation: [https://docs.geoserver.org/stable/en/developer/](https://docs.geoserver.org/stable/en/developer/)

Die beiden Links verweisen auf die Dokumentationen der letzten stabilen Version.
Das *stable* in der URL kann auch durch eine Versionsnummer ersetzt werden, falls
man die Dokumentation einer bestimmten GeoServer-Version aufrufen möchte. Im Rahmen
dieses Workshops wird die **Version {{ book.geoServerVersion }}** behandelt, die resultierende
URL der Benutzerdokumentation würde also <https://docs.geoserver.org/stable/en/user/>
lauten.

![GeoServer-Weboberfläche nach erfolgreichem Login](../assets/geoserver_login_gui.png)

Üblicherweise wird der GeoServer für einen Produktivbetrieb als (Java-)Standalone-Servlet
in Form einer `.war` - Datei bereitgestellt, welche unter <http://geoserver.org/download/>
heruntergeladen werden kann. Die `.war` - Datei muss anschließend auf einem
Servlet-Container (bspw. [Tomcat](https://tomcat.apache.org/) oder
[Jetty](https://eclipse.org/jetty/)) veröffentlicht werden (häufig auch *deploy* genannt). Anschließend
kann die Weboberfläche des GeoServers über den Browser aufgerufen werden.

Weitere Details zur klassischen WAR-Installation finden sich
[hier](https://docs.geoserver.org/stable/en/user/installation/war.html).


> **INFO**
>
> Der GeoServer ist auf dem OSGeoLive-System bereits vorinstalliert und kann im
> Rahmen des Workshops unter {{ book.geoServerBaseUrl }} aufgerufen werden
> (siehe [hier](../environment/README.md)). Diese Variante unterscheidet sich von
> dem klassischen *Deployment* als .war-Datei, da hier ein Java-Programm
> (start.jar) ausgeführt wird, welches programmatisch einen Jetty-Server mit dem
> Geoserver startet. Für die Inhalte des Workshops ist dies aber nicht von Bedeutung.

Im [Folgenden](../ui/index.html) erhalten wir zunächst einen Überblick über die Administrationsoberfläche von GeoServer. Dabei werden wir auf allgemeine Informationen zu den Servereinstellungen, zur Protokollierung sowie auf Sicherheitsaspekte eingehen. Des Weiteren werden wir uns mit dem Menüpunkt *Daten* näher beschäftigen.
