# ❓ Git Commit und Push in Visual Studio

Um Regelmässig deine Änderungen auf den Git Server zu pushen, kannst du direkt im Visual Studio committen und pushen.

* Öffne dazu den Team Explorer. Wenn er noch nicht da ist, findest du ihn unter "View &gt; Team Explorer".
* Klicke auf Changes. 

![](../.gitbook/assets/image%20%28128%29.png)

Nun erscheint eine Auflistung aller Änderungen seit dem letzten Commit. Um diese zu committen, musst du sie zuerst stagen.

![](../.gitbook/assets/image%20%2878%29.png)

* Klicke auf das + Icon, um die Änderungen zu stagen.

![](../.gitbook/assets/image%20%2850%29.png)

* Gebe in die gelbe Textbox einen Text ein, der gut und knapp beschreibt, was du seit dem letzten commit gemacht hast.
* Klicke jetzt auf den kleinen Pfeil neben "Commit Staged" und wähle "Commit Staged and Push"

![](../.gitbook/assets/image%20%287%29.png)

{% hint style="info" %}
Wenn du aus versehen auf "Commit All" geklickt hast, musst du noch manuell einen push durchführen.

* Gehe dazu zurück auf die Hauptansicht des Team Explorers und wähle Sync.
* Unter "Outgoing Commits" klicke auf Push.
{% endhint %}



Diesen Vorgang solltest du regelmässig wiederholen.



## Git in der Konsole

Dies war eine Anleitung, um Git direkt in Visual Studio zu verwenden. Wenn du lieber git in der Konsole verwenden möchtest, findest du in diesem Dokument eine Hilfestellung:

{% file src="../.gitbook/assets/git-anleitung-m318.pdf" caption="Git Anleitung M318" %}

