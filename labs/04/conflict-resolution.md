# Merge Konflikt erzweingen

Dateiinhalt bio.md im Branch main und feature-Facts ändern und committen und dann den Merge versuchen. Nun Merge versuchen, Resultat ist ein Merge Konflikt:

```bash
$ git merge feature-bio
Auto-merging labs/04/bio.md
CONFLICT (content): Merge conflict in labs/04/bio.md
Automatic merge failed; fix conflicts and then commit the result.
```

In der Datei bio.md im main branch, wo der Merge Konflikt ist, steht nun:

```bash
Jonas Weber wuchs in einem kleinen Bergdorf auf und verbrachte seine Kindheit damit, die umliegenden Wälder zu erkunden. Schon früh entwickelte er ein Talent für Musik und begann mit zehn Jahren, eigene Melodien auf der Gitarre zu komponieren. Nach seinem Abschluss in Ingenieurwissenschaften reiste er um die Welt, um verschiedene Kulturen und Musiktraditionen kennenzulernen. Zurück in seiner Heimatstadt gründete er ein kleines Studio, in dem er junge Musiker:innen förderte. Heute ist Jonas als Komponist und Mentor bekannt und inspiriert weiterhin mit seiner Leidenschaft für Klang und Kreativität.
<<<<<<< HEAD
Neue Zeile die nicht in bio.md in branch feature.bio steht hinzufügen, u Merge Konflikt zu provozieren
=======
Merge Konflikt erzwingen mit Änderungen an der Datei bio.md in diesem Branch (feature-bio)
>>>>>>> feature-bio
```

Der Text zwischen den < und = Zeichen ist der geänderte Teil aus der der bio.md im branch main und der Text zwischen den = und > Zeichen der geänderte Teil aus der bio.md im feature-bio branch. Ich kann nun den einen Teil oder anderen Teil behalten oder beide drinne lassen und muss alle >,< und = Zeichen rausnehmen. Ich hab nur den Teil im branch main stehengelassen und die Zeichen des Merge Konfliktes rausgelöscht, damit ist der Merge Konflikt behoben. Anschließend comitted und auf den remote Repo gepusht. 
