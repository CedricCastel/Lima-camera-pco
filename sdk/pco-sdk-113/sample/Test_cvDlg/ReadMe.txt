



  



//TODO:

SetWindowPos(NULL, 100, 100, 200, 100, SWP_NOZORDER); 

CLutTabSliderSheet.hwnd_parent











DDX_Text(pDX, IDC_MINVAL, m_minval);
DDV_MinMaxInt(pDX, m_minval, 0, 65534);






ON_EN_SETFOCUS(IDC_MINVAL, OnSetfocusMinval)
ON_EN_KILLFOCUS(IDC_MINVAL, OnKillfocusMinval)
ON_EN_UPDATE(IDC_MINVAL, OnUpdateMinval)
ON_NOTIFY(UDN_DELTAPOS, IDC_MIN_UPD, OnDeltaposMinUpd)



  DDX_Control(pDX, IDC_MIN_UPD, C_minupd);
  DDX_Control(pDX, IDC_MINVAL, C_minval);
  DDX_Text(pDX, IDC_MINVAL, m_minval);
  DDV_MinMaxInt(pDX, m_minval, 0, 65534); 
    
    
    
    
    
  C_minval.Setup(IDC_MINVAL, 100, 0, hlut->max);
  C_minupd.SetRange(0,hlut->size); 
  C_minupd.SetPos(hlut->min);  
    









================================================================================
    MICROSOFT FOUNDATION CLASS-BIBLIOTHEK: Test_cvDlg-Projekt�bersicht
===============================================================================

Der Anwendungs-Assistent hat diese Test_cvDlg-Anwendung f�r Sie 
erstellt. Diese Anwendung zeigt nicht nur die Grundlagen der Verwendung von
Microsoft Foundation Classes, sondern dient auch als Ausgangspunkt f�r das
Schreiben Ihrer Anwendung.

Diese Datei enth�lt eine Zusammenfassung dessen, was Sie in jeder der Dateien
finden, aus denen Ihre Test_cvDlg�Anwendung besteht.

Test_cvDlg.vcproj
    Dies ist die Hauptprojektdatei f�r VC++-Projekte, die mithilfe eines 
    Anwendungs-Assistenten erstellt werden. 
    Sie enth�lt Informationen �ber die Version von Visual C++, in der die Datei 
    erzeugt wurde, sowie Informationen �ber die Plattformen, Konfigurationen und 
    Projektfunktionen, die mit dem Anwendungs-Assistenten ausgew�hlt wurden.

Test_cvDlg.h
    Dies ist die Hauptheaderdatei f�r die Anwendung. Sie enth�lt weitere
    projektspezifische Header (einschlie�lich "Resource.h") und deklariert
    die CTest_cvDlgApp-Anwendungsklasse.

Test_cvDlg.cpp
    Dies ist die Hauptquelldatei der Anwendung, die die CTest_cvDlgApp-
    Anwendungsklasse enth�lt.

Test_cvDlg.rc
    Dies ist eine Auflistung aller Microsoft Windows-Ressourcen, die das
    Programm verwendet. Sie enth�lt die Symbole, Bitmaps und Cursor, die im 
    Unterverzeichnis "RES" gespeichert werden. Diese Datei kann direkt in 
    Microsoft Visual C++ bearbeitet werden. Ihre Projektressourcen befinden sich 
    in 1031.

res\Test_cvDlg.ico
    Dies ist eine Symboldatei, die als Symbol der Anwendung verwendet wird. 
    Dieses Symbol ist in der Hauptressourcendatei "Test_cvDlg.rc" 
    enthalten.

res\Test_cvDlg.rc2
    Diese Datei enth�lt Ressourcen, die nicht von Microsoft Visual C++
    bearbeitet werden. Sie sollten alle Ressourcen, die nicht mit dem
    Ressourcen-Editor bearbeitet werden k�nnen, in dieser Datei platzieren.

/////////////////////////////////////////////////////////////////////////////

F�r das Hauptrahmenfenster:
    Das Projekt enth�lt eine standardm��ige MFC-Schnittstelle.

MainFrm.h, MainFrm.cpp
    Diese Datei enth�lt die CMainFrame�Rahmenklasse, die von
    CFrameWnd abgeleitet wird und alle SDI-Rahmenfunktionen steuert.

res\Toolbar.bmp
    Diese Bitmapdatei wird verwendet, um gekachelte Bilder f�r die Symbolleiste 
    zu erstellen.
    Die urspr�ngliche Symbolleiste und Statusleiste werden in der CMainFrame-
    Klasse erstellt. Bearbeiten Sie diese Symbolleistenbitmap mithilfe des
    Ressourcen-Editors, und aktualisieren Sie das IDR_MAINFRAME TOOLBAR-Array
    in "Test_cvDlg.rc", um Symbolleisten-Schaltfl�chen hinzuzuf�gen.
/////////////////////////////////////////////////////////////////////////////




/////////////////////////////////////////////////////////////////////////////

Weitere Funktionen:

ActiveX-Steuerelemente
    Die Anwendung unterst�tzt die Verwendung von ActiveX-Steuerelementen.

Druck- und Druckvorschauunterst�tzung
    Der Anwendungs-Assistent hat Code generiert, um die Befehle f�r Drucken, 
    Druckeinrichtung und Druckvorschau zu behandeln, indem Memberfunktionen in 
    der CView-Klasse aus der MFC-Bibliothek aufgerufen werden.

/////////////////////////////////////////////////////////////////////////////

Weitere Standarddateien:

"StdAfx.h", "StdAfx.cpp"
    Diese Dateien werden verwendet, um eine vorkompilierte Headerdatei
    (PCH-Datei) mit dem Namen "Test_cvDlg.pch.pch2 und eine 
    vorkompilierte Typendatei mit dem Namen "StdAfx.obj" zu erstellen.

"Resource.h"
    Dies ist die Standardheaderdatei, die neue Ressourcen-IDs definiert.
    Microsoft Visual C++ liest und aktualisiert diese Datei.

Test_cvDlg.manifest
	Anwendungsmanifestdateien werden von Windows XP verwendet, um eine 
	Anwendungsabh�ngigkeit von verschiedenen Versionen paralleler Assemblys zu 
	beschreiben.
	Das Ladeprogramm verwendet diese Informationen, um die entsprechende 
	Assembly aus dem Assemblycache oder privat aus der Anwendung zu laden. Das
	Anwendungsmanifest kann zur Verteilung als externe Manifestdatei
	enthalten sein, die im gleichen Ordner installiert ist wie die ausf�hrbare 
	Datei der Anwendung, oder sie kann in Form einer Ressource in der 
	ausf�hrbaren Datei enthalten sein. 
/////////////////////////////////////////////////////////////////////////////

Weitere Hinweise:

Der Anwendungs-Assistent verwendet "TODO:", um auf Teile des Quellcodes
hinzuweisen, die Sie erg�nzen oder anpassen sollten.

Wenn Ihre Anwendung MFC in einer freigegebenen DLL verwendet, m�ssen Sie die 
MFC-DLLs verteilen. Wenn die Anwendung eine andere Sprache als die des Gebietsschemas 
des Betriebssystems verwendet, m�ssen Sie au�erdem die entsprechenden lokalisierten Ressourcen "MFC80XXX.DLL" verteilen. Weitere Informationen zu diesen beiden Themen 
finden Sie im Abschnitt zum Verteilen von Visual C++-Anwendungen in der MSDN-
Dokumentation.

/////////////////////////////////////////////////////////////////////////////