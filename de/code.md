# Tragen Sie zum TensorFlow-Code bei

Unabhängig davon, ob Sie eine Verlustfunktion hinzufügen, die Testabdeckung verbessern oder einen RFC für eine größere Designänderung schreiben, dieser Teil des Leitfadens für Mitwirkende hilft Ihnen beim Einstieg. Vielen Dank für Ihre Arbeit und Ihr Interesse an der Verbesserung von TensorFlow.

## Bevor Sie beginnen

Bevor Sie Quellcode zu einem TensorFlow-Projekt beitragen, überprüfen Sie bitte die `CONTRIBUTING.md` im GitHub-Repository des Projekts. (Siehe beispielsweise die [Datei CONTRIBUTING.md für das Kernrepo von TensorFlow](https://github.com/tensorflow/tensorflow/blob/master/CONTRIBUTING.md) .) Alle Code-Mitwirkenden müssen eine [Contributor License Agreement](https://cla.developers.google.com/clas) (CLA) unterzeichnen.

Um Doppelarbeit zu vermeiden, lesen Sie bitte die [aktuellen RFCs](https://github.com/tensorflow/community/tree/master/rfcs) und kontaktieren Sie die Entwickler in den TensorFlow-Foren, bevor Sie mit der Arbeit an einer nicht trivialen Funktion beginnen. Wir sind bei der Entscheidung, neue Funktionen hinzuzufügen, etwas wählerisch, und der beste Weg, um zum Projekt beizutragen und zu helfen, besteht darin, an bekannten Problemen zu arbeiten.

## Probleme für neue Mitwirkende

Neue Mitwirkende sollten nach den folgenden Tags suchen, wenn sie nach einem ersten Beitrag zur TensorFlow-Codebasis suchen. Wir empfehlen dringend, dass neue Mitwirkende zuerst „einfache“ und „gute erste Ausgabe“-Projekte angehen; Dies hilft dem Beitragenden, sich mit dem Beitragsworkflow vertraut zu machen, und den Kernentwicklern, sich mit dem Beitragenden vertraut zu machen.

- `good first issue`
- `easy`
- `contributions welcome`

Wenn Sie daran interessiert sind, ein Team zu rekrutieren, um ein umfangreiches Problem oder eine neue Funktion zu lösen, senden Sie bitte eine E-Mail an die [developer@-Gruppe](https://groups.google.com/a/tensorflow.org/forum/#!forum/developers) und lesen Sie unsere aktuelle Liste der RFCs.

## Code-Review

Neue Funktionen, Fehlerbehebungen und alle anderen Änderungen an der Codebasis unterliegen einer Codeüberprüfung.

Die Überprüfung von Code, der als Pull-Request zum Projekt beigetragen hat, ist eine entscheidende Komponente der TensorFlow-Entwicklung. Wir empfehlen jedem, von anderen Entwicklern eingereichten Code zu überprüfen, insbesondere wenn die Funktion wahrscheinlich von Ihnen verwendet wird.

Hier sind einige Fragen, die Sie während des Code-Review-Prozesses beachten sollten:

- *Wollen wir das in TensorFlow?* Ist es wahrscheinlich, dass es verwendet wird? Gefällt Ihnen als TensorFlow-Benutzer die Änderung und Sie möchten sie nutzen? Liegt diese Änderung im Umfang von TensorFlow? Werden die Kosten für die Wartung eines neuen Features seinen Nutzen wert sein?

- *Stimmt der Code mit der TensorFlow-API überein?* Sind öffentliche Funktionen, Klassen und Parameter gut benannt und intuitiv gestaltet?

- *Ist eine Dokumentation enthalten?* Sind alle öffentlichen Funktionen, Klassen, Parameter, Rückgabetypen und gespeicherten Attribute gemäß den TensorFlow-Konventionen benannt und klar dokumentiert? Werden neue Funktionen in der Dokumentation von TensorFlow beschrieben und nach Möglichkeit mit Beispielen illustriert? Wird die Dokumentation richtig gerendert?

- *Ist der Code für Menschen lesbar?* Ist die Redundanz gering? Sollten Variablennamen aus Gründen der Klarheit oder Konsistenz verbessert werden? Sollen Kommentare hinzugefügt werden? Sollten Kommentare als nicht hilfreich oder irrelevant entfernt werden?

- *Ist der Code effizient?* Könnte es leicht umgeschrieben werden, um effizienter zu laufen?

- Ist der Code *abwärtskompatibel* mit früheren Versionen von TensorFlow?

- Wird der neue Code *neue Abhängigkeiten* von anderen Bibliotheken hinzufügen?

## Testen und verbessern Sie die Testabdeckung

Hochwertige Komponententests sind ein Eckpfeiler des TensorFlow-Entwicklungsprozesses. Zu diesem Zweck verwenden wir Docker-Images. Die Testfunktionen werden entsprechend benannt und sind dafür verantwortlich, die Gültigkeit von Algorithmen sowie verschiedene Optionen des Codes zu überprüfen.

Alle neuen Funktionen und Fehlerbehebungen *müssen* eine angemessene Testabdeckung beinhalten. Wir freuen uns auch über Beiträge zu neuen Testfällen oder Verbesserungen an bestehenden Tests. Wenn Sie feststellen, dass unsere bestehenden Tests nicht abgeschlossen sind – auch wenn dies derzeit keinen Fehler verursacht – reichen Sie bitte ein Problem und, wenn möglich, einen Pull-Request ein.

Für die speziellen Einzelheiten der Verfahren in jedem TensorFlow Projekt zu testen, finden Sie in die `README.md` und `CONTRIBUTING.md` Dateien im Projekt - Repo auf GitHub.

Besondere Bedenken bei *angemessenen Tests* :

- Wird *jede öffentliche Funktion und Klasse* getestet?
- Wird ein *vernünftiger Satz von Parametern* , deren Werten, Werttypen und Kombinationen getestet?
- Bestätigen die Tests, dass der *Code korrekt* ist und das *tut, was in der Dokumentation angegeben ist, dass* der Code tun soll?
- Wenn es sich bei der Änderung um eine Fehlerbehebung handelt, ist ein *Nicht-Regressionstest* enthalten?
- Bestehen die Tests *den Continuous Integration* Build?
- Decken die Tests *jede Codezeile ab?* Wenn nicht, sind die Ausnahmen sinnvoll und explizit?

Wenn Sie Probleme finden, ziehen Sie bitte in Betracht, dem Beitragenden zu helfen, diese Probleme zu verstehen und zu lösen.

## Fehlermeldungen oder Protokolle verbessern

Wir freuen uns über Beiträge, die Fehlermeldungen und Protokollierung verbessern.

## Beitragsworkflow

Codebeiträge – Bugfixes, Neuentwicklungen, Testverbesserungen – folgen alle einem GitHub-zentrierten Workflow. Um an der TensorFlow-Entwicklung teilzunehmen, richten Sie ein GitHub-Konto ein. Dann:

1. Forken Sie das Repo, an dem Sie arbeiten möchten. Gehen Sie zur Projekt-Repository-Seite und verwenden Sie die Schaltfläche *Fork.* Dadurch wird eine Kopie des Repositorys unter Ihrem Benutzernamen erstellt. (Weitere Informationen zum Forken eines Repositorys finden Sie in [diesem Handbuch](https://help.github.com/articles/fork-a-repo/) .)

2. Klonen Sie das Repository auf Ihr lokales System.

    `$ git clone git@github.com:your-user-name/project-name.git`

3. Erstellen Sie einen neuen Zweig, um Ihre Arbeit zu speichern.

    `$ git checkout -b new-branch-name`

4. Arbeiten Sie an Ihrem neuen Code. Tests schreiben und ausführen.

5. Bestätigen Sie Ihre Änderungen.

    `$ git add -A`

    `$ git commit -m "commit message here"`

6. Übertragen Sie Ihre Änderungen per Push in Ihr GitHub-Repository.

    `$ git push origin branch-name`

7. Öffnen Sie einen *Pull-Request* (PR). Rufen Sie das ursprüngliche Projekt-Repository auf GitHub auf. Es wird eine Nachricht zu Ihrem kürzlich gepushten Branch angezeigt, in der Sie gefragt werden, ob Sie einen Pull-Request öffnen möchten. Folgen Sie den Anweisungen, *vergleichen* Sie die Repositorys und senden Sie die PR. Dadurch wird eine E-Mail an die Committer gesendet. Sie können in Erwägung ziehen, eine E-Mail an die Mailingliste zu senden, um mehr Sichtbarkeit zu erzielen. (Weitere Informationen finden Sie im [GitHub-Leitfaden zu PRs](https://help.github.com/articles/creating-a-pull-request-from-a-fork) .

8. Betreuer und andere Mitwirkende werden *Ihre PR überprüfen* . Bitte nehmen Sie an der Konversation teil und versuchen Sie, *die gewünschten Änderungen vorzunehmen* . Sobald die PR genehmigt wurde, wird der Code zusammengeführt.

*Bevor Sie an Ihrem nächsten Beitrag arbeiten* , stellen Sie sicher, dass Ihr lokales Repository auf dem neuesten Stand ist.

1. Stellen Sie die Upstream-Fernbedienung ein. (Sie müssen dies nur einmal pro Projekt tun, nicht jedes Mal.)

    `$ git remote add upstream git@github.com:tensorflow/project-repo-name`

2. Wechseln Sie in den lokalen Master-Zweig.

    `$ git checkout master`

3. Ziehen Sie die Änderungen aus dem Upstream herunter.

    `$ git pull upstream master`

4. Übertragen Sie die Änderungen auf Ihr GitHub-Konto. (Optional, aber eine gute Übung.)

    `$ git push origin master`

5. Erstellen Sie eine neue Filiale, wenn Sie eine neue Arbeit beginnen.

    `$ git checkout -b branch-name`

Zusätzliche `git` und GitHub-Ressourcen:

- [Git-Dokumentation](https://git-scm.com/documentation)
- [Git-Entwicklungsworkflow](https://docs.scipy.org/doc/numpy/dev/gitwash/development_workflow.html)
- [Auflösen von Zusammenführungskonflikten](https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/) .

## Checkliste für Mitwirkende

- Lesen Sie die Richtlinien für Beiträge.
- Lesen Sie den Verhaltenskodex.
- Stellen Sie sicher, dass Sie die Contributor License Agreement (CLA) unterzeichnet haben.
- Prüfen Sie, ob Ihre Änderungen den Richtlinien entsprechen.
- Überprüfen Sie, ob Ihre Änderungen mit dem TensorFlow-Codierungsstil übereinstimmen.
- Führen Sie Komponententests durch.
