---
title: Instal·lació de les dades d'exemple
description: Aquest tema proporciona informació sobre la instal·lació de les dades d'exemple al Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 3c9cca7aa9d85bb38e48820b361ba07923ceddbd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132411"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instal·lació de les dades d'exemple per a l'aplicació del Project Service

Per ajudar-vos a crear els vostres propis entorns de demostració, Microsoft proporciona paquets de dades d'exemple que es poden descarregar que mostren les capacitats de les vostres aplicacions. Hi ha dos tipus de paquets de dades d'exemple:
- Dades de configuració/referència
- dades de demostració (dades transaccionals i de referència/configuració, com ara ordres de treball i projectes)

Els paquets de dades de **referència** d'exemple es poden descarregar en tres paquets diferents, de manera que podeu instal·lar dades només per al Project Service, o només per al Field Service, o per a totes dues aplicacions alhora.

Els paquets de dades de configuració/referència d'exemple són:

- [**V902PSMasterData** - només versió 3.x del Project Service](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - només versió 8.x del Field Service](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x i Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

El paquet de dades de **demostració** més recent és:

 - [**FPSDemoData** - Field Service 8.x i Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Les instruccions d'instal·lació difereixen lleugerament en els usuaris per crear i configurar la secció però la resta és igual que en la [**publicació del blog**](https://aka.ms/fpsdemodatablog) anterior. Aquest paquet ofereix un conjunt de dades de demostració reduït i triga aproximadament 3 hores a instal·lar-se.

Aquests paquets de dades d'exemple només estan disponibles en anglès.

> [!IMPORTANT]
> **No hi ha cap manera de desinstal·lar les dades d'exemple.** Només heu d'instal·lar aquests paquets en sistemes demostració, avaluació, formació o prova. Tingueu en compte també que la instal·lació d'un paquet individual i la instal·lació posterior d'un altre paquet individual no són compatibles. (En altres paraules, no podeu instal·lar **FSMasterData** seguit de **PSMasterData**, o viceversa). Si veieu que necessiteu dades d'exemple per a ambdues aplicacions en qualsevol moment del futur, heu d'instal·lar el paquet **v902FPSMasterData**.

Quan instal·leu algun dels paquets de dades d'exemple, el procés d'instal·lació realitza les accions següents:

- Crea o estableix paràmetres predeterminats per utilitzar el Project Service, el Field Service o ambdues aplicacions (si s'escau).

- Importa dades d'exemple de les aplicacions, com ara recursos que es poden reservar, funcions específiques de l'aplicació, vendes i llistes de preus de cost, unitats organitzatives, registres de processos de vendes i altres entitats per demostrar les funcions clau.  

Amb el paquet de **dades de demostració**, obtindreu les dades transaccionals anteriors i addicionals, com ara ordres de treball i projectes.

Us interessa saber quines funcions podeu demostrar amb les dades d'exemple? Vegeu l'escenari fictici Fabrikam Robotics a les [notes tècniques](#technical-notes).

Si teniu preguntes sobre com instal·lar aquests paquets de dades d'exemple, envieu-nos un correu electrònic a [fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Requisits

El protocol d'instal·lació dóna per fet la informació sobre la vostra instància de destinació (org):

- La llengua de base és l'anglès i la moneda base és el dòlar dels Estats Units (USD, $).

- L'organització no té dades del Project Service ni del Field Service, o només té les dades predeterminades de barebones que venien amb les noves organitzacions.

- Ja està instal·lada la versió correcta de l'aplicació de negoci:
       
    - **Per a FPSDemoData o v902FPSMasterData:** l'organització té la versió 8.x del Field Service i la versió 3.x del Project Service instal·lada.

    - **Per a v902PSMasterData:** l'organització té la versió 3.x del Project Service instal·lada.

    - **Per a v902FSMasterData:** l'organització té la versió 8.x del Field Service instal·lada.

> [!NOTE]
> Si heu d'instal·lar les dades d'exemple en un entorn de prova del Project Service o del Field Service que ja tingui dades (no es recomana), haureu de suspendre les comprovacions prèvies de seguretat que realitza l'instal·lador. Per obtenir més informació, consulteu les notes tècniques següents.

## <a name="prepare-for-installation"></a>Prepareu-vos per a la instal·lació

Cal que executeu l'instal·lador en un ordinador amb una versió recent del Windows (es prefereix el Windows 10).

Heu de comptar amb que l'ordinador romangui connectat a una xarxa i que la instal·lació dura fins a **1 hora** per a les **dades de configuració/referència**. (Normalment, la instal·lació triga uns 30 minuts per al **FPSMasterData**, que inclou dades d'exemple per a ambdues aplicacions.) Per al **FPSDemoData**, la instal·lació trigarà aproximadament **3 hores**.

L'ordinador hauria de tenir desactivada la funció de protector de pantalla. En cas contrari, si s'activa el protector de pantalla, es poden perdre les credencials de sessió de la instal·lació (a menys que mantingueu activa la vostra sessió).

> [!div class="mx-imgBorder"]
> ![Captura de pantalla de la configuració del protector de pantalla, amb el protector de pantalla desactivat](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Descarregar i desempaquetar

L'instal·lador de dades d'exemple del Project Service i del Field Service es distribueix com un executable autoextraïble. Els noms dels fitxers poden variar segons el paquet de dades d'exemple, però els passos segueixen essent iguals i no importa quin paquet instal·leu.

Després de descarregar un paquet, executeu el fitxer .exe i, a continuació, accepteu els termes i condicions per desempaquetar el fitxer zip comprimit. A continuació, heu d'extreure el contingut d'aquest fitxer a una carpeta de l'ordinador.

Segons el sistema operatiu i la configuració de seguretat, és possible que hàgiu de seguir els següents passos després de desempaquetar el fitxer zip:

1. Cerqueu i feu clic dret al fitxer **FPSDemoData.dll** de la carpeta **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Trieu **Desbloqueja**.

3. Seleccioneu **Aplica**.

4. Seleccioneu **D'acord**.


## <a name="create-or-configure-users"></a>Crear o configurar els usuaris

El paquet **FPSDemoData** requereix sis usuaris mentre que el paquet **FPSMasterData** només en requereix un. Consulteu quin és el correcte per al vostre paquet de dades d'exemple.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Crear o configurar usuaris: paquets de dades de configuració/referència

El paquet **FPSMasterData** està dissenyat per instal·lar-se amb un usuari anomenat Spencer Low amb els paràmetres que es descriuen aquí. Per instal·lar el paquet correctament, heu de crear (o canviar el nom de manera temporal) usuaris al vostre entorn per fer coincidir la configuració de dades d'exemple entrant.

Per crear o configurar usuaris, aneu a **Configuració** > **Seguretat** > **Usuaris** i feu el següent:

1. Establiu UserFullname="Spencer Low" amb el nom d'usuari "spencerl" (**minúscules**) a les funcions de l'Administrador de projectes i del Cap de pràctiques.

2. Seleccioneu l'usuari **Spencer Low** i, a continuació, **Administra les funcions**. Cerqueu i seleccioneu la funció **Administrador del sistema** i, a continuació, seleccioneu **D'acord** per concedir drets d'administració complets a Spencer Low. Aquest pas és necessari per assegurar que es creïn registres d'exemple amb la propietat correcta de l'usuari i, per tant, es mostrin correctament les vistes.

3. Des del paquet descarregat, cal actualitzar un fitxer d'assignació de dades amb adreces de correu electrònic del context d'usuari predeterminat. Per fer-ho, obriu **PkgFolder** i, a continuació, cerqueu i obriu el fitxer **ImportUserMapFile.xml** al Bloc de notes (o a Visual Studio o un altre editor XML). Establiu el camp **DefaultUserToMapTo=** a l'adreça de correu electrònic de l'usuari Spencer Low.

4. Si no esteu utilitzant Spencer Low amb el nom d'usuari **spencerl**, heu d'actualitzar un fitxer addicional. Obriu el fitxer **DemoDataPreImportConfig.xml** i, a continuació, cerqueu l'etiqueta **userstocreateandconfigure**. Actualitzeu l'etiqueta **\<login\>** amb el nom d'usuari del vostre usuari Jordi Lluch. Per obtenir informació addicional, consulteu les [notes tècniques](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Crear o configurar usuaris: paquet de dades de demostració

El paquet de dades de demostració requereix sis usuaris. Per instal·lar correctament el paquet, feu el següent:

 1. Creeu o reanomeneu temporalment els usuaris existents perquè coincideixin amb la configuració de les dades d'exemple des de **Configuració** > **Seguretat** > **Usuaris**.
 
    Aquestes funcions només són necessàries per a demostracions basades en persones.  
    - Nom complet de l'usuari = "David So" com a tècnic del Field Service   
    - Nom complet de l'usuari = "Jamie Reding" com a distribuïdor del Field Service i el Customer Service   
    - Nom complet de l'usuari = "Molly Clark" com a administradora del compte   
    - Nom complet de l'usuari = "Spencer Low" com cap de pràctiques i projectes  
    - Nom complet de l'usuari = "Veronica Quek" com a membre de l'equip   
    - Nom complet de l'usuari = "William Contoso"
  
2. Per importar les dades de demostració, assigneu als sis usuaris anteriors la funció d'administrador per tal que els registres d'exemple s'importin correctament. 

3. Obriu **PkgFolder** i, a continuació, cerqueu i obriu **ImportUserMapFile.xml**. Actualitzeu els camps **Nou=** per a les adreces de correu electrònic dels usuaris corresponents al sistema.

   > [!div class="mx-imgBorder"]
   > ![Captura de pantalla de l'UserMapFile](media/sample-data-7.png)

4. Si el nom complet de l'usuari "Spencer Low" té un identificador d'usuari diferent a **"spencerl"**, heu d'actualitzar un fitxer addicional. Obriu **DemoDataPreImportConfig.xml** i cerqueu l'etiqueta **userstocreateandconfigure**. Actualitzeu l'etiqueta **\<login\>** amb el loginId (distingeix les majúscules de les minúscules). 

5. El calendari del primer usuari (a l'etiqueta **userstocreateandconfigure**) s'utilitza per emplenar les hores de feina de tots els recursos que es poden reservar en la importació de les dades de demostració. Aneu a **Configuració** > **Seguretat** > **Usuaris**, busqueu l'usuari "Spencer Low" i obriu l'opció "Hores de feina". Editeu les hores de feina existents, seleccioneu l'opció **Tota la planificació setmanal periòdica de principi a fi**. Assegureu-vos que **les hores de feina estan definides de 8:00 a 17:00 (9 hores), de dilluns a divendres i amb la zona horària definida com a hora del Pacífic (EUA i Canadà)**. Aquesta acció és necessària per garantir que el tauler de projecte i planificació es mostri correctament.

**Recomanació**: penseu a crear una còpia de seguretat de la vostra organització en aquest moment, per si necessiteu tornar al punt d'inici si alguna cosa surt malament durant la instal·lació de les dades d'exemple. Per obtenir més informació, consulteu [Restaurar i realitzar còpies de seguretat d'instàncies](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Executeu l'Package Deployer

1. Cerqueu i executeu **PackageDeployer.exe** a la carpeta **v902FPSMasterData** o **PackageDeployer_FPSDemoData**.

2. Accepteu les condicions.

3. A la finestra següent:

   a. Seleccioneu el tipus d'implementació de l'**Office 365**.

   b. Utilitzeu l'usuari i la contrasenya de l'usuari administrador del sistema configurat a "Crear o configurar usuaris" ("Spencer Low" amb el nom d'usuari "spencerl").

   c. Assegureu-vos que la casella **Mostra la llista d'organitzacions disponibles** està seleccionada.

      > [!div class="mx-imgBorder"]
      > ![Captura de pantalla de la finestra del Package Deployer amb l'opció "Visualitza la llista d'organitzacions disponibles" seleccionada](media/sample-data-2.png)

4. Seleccioneu l'organització on voleu instal·lar les dades d'exemple.

5. Seleccioneu **Següent** fins que vegeu el quadre de diàleg **Configura les dades de demostració**.

   > [!div class="mx-imgBorder"]
   > ![Captura de pantalla de la finestra que mostra l'estat de l'instal·lador de les dades de demostració](media/sample-data-3.png)

6. Abans de continuar, tingueu en compte que la instal·lació de dades d'exemple pot trigar fins a una hora (normalment ~10 minuts). Haureu d'assegurar-vos que l'ordinador roman encès i connectat a una xarxa durant tot el procés d'instal·lació i que la vostra sessió roman activa.   

7. Quan estigueu a punt, feu clic a **Següent** per iniciar el procés d'instal·lació de dades d'exemple. Després de carregar les dades d'exemple, feu clic a **Finalitza**.

## <a name="verify-the-sample-data-installation"></a>Comprovar la instal·lació

Per comprovar l'estat, verifiqueu que la quantitat de registres i tipus d'entitats que figuren en l'escenari fictici de Fabrikam Robotics apareixen com s'esperava.

Després que les dades d'exemple es carreguin completament, inicieu la sessió com a usuari Spencer Low i confirmeu el següent:

- Si s'ha instal·lat l'aplicació del Project Service, aneu al **Project Service** > **Configuració** > **Llistes de preus**. Confirmeu que hi ha índexs de facturació i costos amb la moneda adequada per a cada país/regió del conjunt de dades.

- Si s'ha instal·lat l'aplicació del Project Service, aneu al **Universal Resource Scheduling** > **Configuració** > **Unitats organitzatives**. Confirmeu que s'ha associat una llista de preus de cost amb la moneda adequada a cada unitat organitzativa (excloses les entrades de la ciutat). Si n'hi falten, busqueu i associeu la llista de preus de cost correcta.

- Si s'ha instal·lat l'aplicació del Field Service, aneu al **Project Service** > **Configuració** > **Llistes de preus**. Confirmeu que els índexs de facturació i cost siguin correctes. Aneu al **Field Service** > **Configuració** > **Llistes de preus** i comproveu que les tarifes de facturació i cost tenen configurada la moneda adequada per a cada país/regió del conjunt de dades.

  > [!div class="mx-imgBorder"]
  > ![Captura de pantalla de les llistes de preus actives](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Captura de pantalla de les unitats de organitzatives actives](media/sample-data-5.png)

## <a name="technical-notes"></a>Notes tècniques

Consulteu a continuació com obtenir més detalls tècnics sobre la instal·lació d'aquestes dades.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instal·lar dades d'exemple i sobreescriure les dades existents (no es recomana)

Si heu d'instal·lar les dades d'exemple en un entorn de prova del Field Service o del Project Service que ja tingui dades, haureu de suspendre les comprovacions prèvies de seguretat que realitza l'instal·lador.

Per fer-ho, aneu a la carpeta **PkgFolder** per trobar i obrir el fitxer **DemoDataPreImportConfig.xml** amb el Bloc de notes (o un altre editor XML).

Cerqueu el valor següent i, a continuació, canvieu la configuració de true a false:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Aquest canvi fa que l'instal·lador passi per alt algunes comprovacions importants de seguretat, com ara:

- Confirmar que no hi ha més d'un registre d'**unitat organitzativa** actiu i, a continuació, canviar-ne el nom a **Fabrikam US**.

- Confirmar que no hi ha més d'un registre de **Plantilla de treball** actiu.

- Confirmar que no hi ha més d'un registre de **Paràmetres de projecte** actiu i, a continuació, canviar el nom d'aquesta entrada a **Paràmetres**.

### <a name="configuration-components"></a>Components de configuració

Hi ha altres components de configuració en aquest fitxer de configuració previ a la importació. Per als usuaris tècnics, alguns són:

- **\<RequiredSolutions\>** especifica les instal·lacions de solucions de requisits previs i els seus números de versió.

- **\<InstallSampleData\>** controla si hi ha instal·lades les dades d'exemple de fàbrica a les aplicacions.

    - false: elimina la instal·lació d'aquestes dades incorporades (les que es poden suprimir)

    - true: instal·la les dades incorporades concurrents amb la instal·lació de les dades d'exemple de FS i PSA

- **\<PreImportDataCollection\>** especifica les assignacions de dades de fitxers plans i els registres associats que s'han d'importar abans de la instal·lació principal de dades d'exemple.

- **\<EntitiesToEnableScheduling\>** especifica quines entitats s'han d'habilitar per a la Reserva al Microsoft Dynamics Scheduling (àlies Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** especifica els recursos reservables que es crearan (si encara no existeixen) abans d'executar la importació de dades d'exemple. Tingueu en compte que el sistema d'origen mostra les dades del recurs que es pot reservar que coincideixen amb els registres del sistema de destinació en FullName i inici de sessió de cada recurs. Per tant, NO és possible canviar els noms d'aquest fitxer de configuració prèvia a menys que primer importeu les dades d'exemple en un sistema de destinació que utilitzi aquests noms i, a continuació, canvieu el nom dels recursos que es poden reservar al nom desitjat juntament amb els registres d'Usuaris habilitats i, a continuació, exporteu les dades una altra vegada per importar al vostre sistema de destinació final (i actualitzeu les entrades antigues i noves del **ImportUserMapFile.xml** segons correspongui).

- **\<PluginsToDisable\>** especifica complements d'elements de línia molt discrets que s'han de desactivar durant la importació de dades d'exemple i després tornar a activar.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Escenari fictici Fabrikam Robotics

Els paquets de dades de referència d'exemple del Field Service i del Project Service instal·len la **solució Fabrikam Manufacturing Master Data (v3.0.0.0)**, juntament amb aproximadament 4.000 registres i 40 entitats diferents. Els paquets de dades d'exemple separats per al Field Service o el Project Service contenen un subconjunt de dades d'exemple **v902FPSMasterData** per a aquesta aplicació. El paquet **Dades de demostració** instal·la la **solució Fabrikam Manufacturing Demo Data (v3.0.0.7)** amb aproximadament 22.000 registres d'entre 148 entitats.

L'empresa fictícia, Fabrikam Robotics, és fabricant de robots de línia de muntatge de dispositius electrònics i és coneguda per la qualitat del producte, la innovació i el servei al client sòlid, inclosa la planificació de la instal·lació, la implementació i els serveis de manteniment en curs. Fabrikam té la seu als Estats Units (Fabrikam EUA) i té operacions de servei basades en projectes a França, Índia, Regne Unit i Suïssa.

Les operacions del Field Service se centren als Estats Units, principalment a la zona més gran de Seattle. La companyia se centra en aprofitar la connectivitat de l'Internet de les coses (IoT) per supervisar el rendiment dels actius dels clients i oferir serveis cada vegada més proactius.

La descripció següent, és una descripció general detallada de les dades d'exemple:

- Elements de dades d'exemple comuns (inclosos per a ambdues aplicacions)

    - 1 usuari

    - 71 comptes

    - 137 contactes

    - Diversos tipus de transaccions i categories

    - 50 productes amb 1 llista de preus de productes

    - 14 llistes de preus/costos

    - 31 característiques (aptituds del recurs) en 2 models de classificació amb 3 nivells (valors de classificació)

- Project Service

    - 8 unitats organitzatives

    - 6 nivells d'utilització de funcions específiques

    - Més de 2800 especificacions funció-preu

- Field Service

    - 4 zones de vendes

    - 5 tipus d'ordre de treball

    - 22 actius del client

    - 9 tipus d'incidents amb un ventall de característiques de recursos associats (9), serveis (13) i tasques de servei (13)
   
El paquet **Dades de demostració** instal·la aproximadament 179 ordres de treball, 12 projectes i les dades transaccionals associades. 

### <a name="change-the-work-hours-for-sample-resources"></a>Canviar l'horari laboral dels recursos d'exemple

De manera predeterminada, tots els recursos que es poden reservar tenen un calendari de 24 hores laborables.

Si heu de canviar l'horari laboral per obtenir recursos d'exemple que es poden reservar, aneu a **Universal Resource Scheduling** > **Programació** > **Recursos**.

Seleccioneu un usuari (per exemple, Spencer Low) i canvieu-li l'horari laboral a les hores que voleu aplicar a diversos usuaris. Aneu a **Universal Resource Scheduling** > **Configuració** > **Plantilles d'hores de feina** i editeu el registre de **Plantilla de treball per defecte**. Al camp **Recursos de plantilla**, seleccioneu un usuari amb les hores de feina que voleu aplicar a altres recursos. Aneu a **Universal Resource Scheduling** > **Planificar** > **Recursos** > **Recursos que es poden reservar actius**. Seleccioneu els recursos que voleu canviar i, a continuació, seleccioneu **Establir calendari**. A la llista desplegable **Plantilla de treball**, seleccioneu la plantilla **Hores de feina per defecte** o una altra plantilla amb el recurs de plantilla correcte. Quan aneu al tauler de programació, heu de veure que ara els recursos tenen hores de feina actualitzades.

> [!div class="mx-imgBorder"]
> ![Captura de pantalla de recursos actius que es poden reservar](media/sample-data-6.png)
