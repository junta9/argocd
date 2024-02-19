## Creation d'une application kubernetes + Manifest

### Créez un repo github public contenant votre chart Helm qui sera composée comme telle:

1 pvc avec storage class pour création d'un volume automatisé
1 deployement nginx, qui montera ce volume dans /usr/share/nginx/html/
1 service LoadBalancer permettant de consulter l'application.
1 cronjob qui s'execute toutes les heures et qui affiche l'heure à l'aide de la commande date (on utilisera l'image busybox).

### Créez votre application dans ArgoCD (via interface graphique):

Créez un repository pour permettre de synchroniser votre repo git helm (dans settings)
Créez un projet (dans settings), précisez bien en cible le cluster local, et votre namespace personnel
Dans Application créez une application, cette application sera synchronisée en automatique dans votre namespace personnel.

Une fois l'application créée et synchronisée, regarder dans votre namespace à l'aide de la commande kubectl les objets créés.
Supprimez le déploiement dans votre namespace à l'aide de la commande kubectl et observez le comportement dans argocd.


