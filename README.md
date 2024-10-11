# MainsdOeuvres

machineAetat :
  Ce patch gère les transitions entre les etats, il doit simplement etre lancer et tourne tout seul ensuite.
  Il emet sur le port 4000
  Pour qu'il envoie les etat en OSC il faut ouvrir le sous patch OSCsend et ajouter un udpsend pour chaque machine qui souhaite recevoir l'info.

receiveEtat :
  Ce patch est à integrer dans vos patch max qui devrait recevoir les etats.
  Il faut simplement le mettre dans un bpatcher et enclenché le bouton Listen pour qu'il ecoute l'osc sur le port 4000

Light :
  Un patch qui communique en osc avec Onyx.
  La communication se fait en localhost sur le port 7401

MainO.OnyxShow :
  Une sauvegarde qu'il faut load a l'ouverture d'Onyx.
  Il faudra surement reconfigurer l'osc dans onyx en allant dans les reglages.
  Sur la page OSC rentrer comme port 7401
  Sur la page device activer un device avec comme adresse IP l'adresse de la machine sur laquelle le patch Light fonctionne (on ne peut pas rentrer 127.0.0.1 donc si c'est la meme machine qui gere max et onyx il faut quand meme rentrer son adresse sur le reseau)
