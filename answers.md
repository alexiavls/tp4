# Answers

Nom : Valais
Prénom : Alexia
NB : 1

# 1.
A quoi sert l'A/B testing ?
L'A/B testing permet de tester deux versions différentes sur les utilisateurs. On met en place en parallèle chacune des solutions sur un échantillon de testeurs et on analyse l'impact de chacune. La plus efficace sera préférée.

Comment appliquer de l'A/B testing grâce à Istio ?

# 2.
Comment simuler un problème de timeout avec Istio ?

Comment le résoudre ?

# 3.
Qu'est-ce que le canary release ?
Le canary release permet de tester une nouvelle version auprès qu'une part restreinte d'utilisateurs. 

En quoi est-ce utile ?
Cela permet de détecter des erreurs ou des dysfonctionnement avec le déploiement auprès de la totalité des utilisateurs. Les retours sont plus rapides et il est plus facile de revenir à la version précédente. 

Comment l'implémenter dans Istio ?
L'application est hébergée sur deux chaînes applicatives. On déploit la version N+1 sur une des chaînes et conserve la version N sur la seconde.

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un Circuit Breaker permet de maintenir un service même si des erreurs bloquantes apparaissent. Si une erreur est détectée le circuit breaker va arrêter les requètes et envoyer une réponse alternative permettant le bon fonctionnement des autres fonctionnalités. 

Comment l'implémenter dans un contexte Kubernetes ?

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?

# 7.
Pourquoi bloquer le traffic vers un service ?

Comment l'implémenter simplement avec Istio ?

# 8.
Quel est la problématique de tracing distribué ?

Quel est la spécification du tracing distribué et son implémentation dans Istio ?

# 9.
Comment s'appelle l'outil de récupération des métrics ?

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?

# 12.
A quoi sert un servicegraph ?

Quel serait l'utilité dans le quotidien d'un ops ?
