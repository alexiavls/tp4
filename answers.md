# Answers

Nom : Valais
Prénom : Alexia
NB : 1

# 1.
A quoi sert l'A/B testing ?
L'A/B testing permet de tester deux versions différentes sur les utilisateurs. On met en place en parallèle chacune des solutions sur un échantillon de testeurs et on analyse l'impact de chacune. La plus efficace sera préférée.

Comment appliquer de l'A/B testing grâce à Istio ?
On indique une règle de route dans le fichier .yaml

# 2.
Comment simuler un problème de timeout avec Istio ?
On utilise le falt injection.

Comment le résoudre ?
On peut optimiser le code ou modifier le timeout en configurant les applications.

# 3.
Qu'est-ce que le canary release ?
Le canary release permet de tester une nouvelle version auprès qu'une part restreinte d'utilisateurs. 

En quoi est-ce utile ?
Cela permet de détecter des erreurs ou des dysfonctionnement avec le déploiement auprès de la totalité des utilisateurs. Les retours sont plus rapides et il est plus facile de revenir à la version précédente. 

Comment l'implémenter dans Istio ?
L'application est hébergée sur deux chaînes applicatives. On déploit la version N+1 sur une des chaînes et conserve la version N sur la seconde.
On utilise route:destination: host: website subset: version-2 weight: 5 destination: host: website subset: version-1 weight: 95

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un Circuit Breaker permet de maintenir un service même si des erreurs bloquantes apparaissent. Si une erreur est détectée le circuit breaker va arrêter les requètes et envoyer une réponse alternative permettant le bon fonctionnement des autres fonctionnalités. 

Comment l'implémenter dans un contexte Kubernetes ?
On configure les application Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
On fait une copie du trafic sur un "request path" afin de faire des modifications tout en limitant les risques.

# 7.
Pourquoi bloquer le traffic vers un service ?
Cela permet d'éviter les retards et temps de latence. En effet, si le traffic vers un service est trop lent, il va ralentir toute l'application.

Comment l'implémenter simplement avec Istio ?
On limite dynamiquement le trafic avec le "rate limit".
istioctl create -f ratelimit-handler.yaml : configurer le nombre maximum de requêtes par seconde avec un handler
istioctl create -f ratelimit-rule.yaml : fixer le quota memoire (memquota) en activant le rate limit avec le rule

# 8.
Quel est la problématique de tracing distribué ?
Il est difficile de comprendre le comportement d'une application.

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Istio va tracer les appels de chacune des applications du cluster et les afficher sur un dashboard.

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Promotheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana

# 12.
A quoi sert un servicegraph ?
C'est une représentation schématique de l'ensemble des services et des appels.

Quel serait l'utilité dans le quotidien d'un ops ?
L'utilité serait de visualiser l'ensemble des services.
