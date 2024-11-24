# Code inefficace

Parfois, nous écrivons tout simplement du mauvais code. Cela peut être dû à des erreurs d'inattention, à une mauvaise compréhension des langages de programmation, à un manque de temps, à un manque de concentration ...

Sur les puissants processeurs d'aujourd'hui, les cas individuels de tels problèmes sont à peine perceptibles. Cependant, accumulés des milliers ou des millions de fois, ils peuvent avoir un impact considérable sur les performances. 

Voici quelques exemples typiques :

- Effectuer trop de divisions. La division est une opération coûteuse pour un processeur !
- Effectuer trop de calculs de racine carrée - là aussi, c'est très coûteux !
- Trop de branches ou des branches inutiles dans notre code
- Trop d'allocations et de désallocations de mémoire qui nécessitent des frais généraux de maintenance
- ...


{% hint style="success" %}
Même si nous évitons d'optimiser trop tôt, il faut trouver un bon équilibre entre l'optimisation précoce et l'écriture d'un code efficace. Cela se fait surtout avec l'expérience.

Cependant, une règle à suivre est de toujours remettre en question le code que vous écrivez ! S'agit-il d'une allocation inopportune ? Peut-être puis-je réutiliser une variable déclarée dans une portée supérieure, plutôt que de recréer une nouvelle variable à chaque itération de la portée. Puis-je reformuler un calcul pour éviter une division ou une racine carrée ?
{% endhint %}

## Opérations mathématiques coûteuses

Sur les puissants processeurs d'aujourd'hui et avec les compilateurs modernes avancés, nous pouvons parfois ignorer superbement les techniques d'optimisation courantes à l'échelle la plus basse.

### Division

Il est parfois possible d'optimiser notre code en multipliant par une décimale plutôt qu'en divisant par un grand nombre :

[Which is better? Divide by 2 or multiply by 0.5?](https://www.ibm.com/support/pages/which-better-divide-2-or-multiply-05)

{% hint style="warning" %}
Cependant, une fois de plus, il faut se méfier de l'optimisation précoce !

[Here is the tip: Beware of performance tips](https://www.ibm.com/support/pages/node/1119393)

{% endhint %}

### La racine carrée

La racine carrée est une opération coûteuse, et peut parfois être évitée !

Par exemple, dans notre raytracer, nous calculons souvent la longueur d'un vecteur en utilisant pythagore :

$$
h^2 = x^2 + y^2
$$

Ou bien : 

$$
h = \sqrt{x^2 + y^2}
$$

Par exemple, si nous calculons la longueur de deux vecteurs afin de pouvoir comparer leurs longueurs, nous pouvons éviter d'utiliser la racine carrée et nous contenter de comparer les valeurs au carré !

Par exemple, nous avons deux vecteurs `A` et `B` dont les longueurs sont `3` unités et `4` unités. En utilisant la longueur réelle ou la longueur au carré, nous pouvons toujours déterminer que `A` est plus court queb `B`.


$$
3^2 = 9
$$

$$
4^2 = 25 
$$

Nous savons que :

$$
3 < 4
$$

Mais aussi :

$$
9 < 16
$$

Ainsi, que nous comparions la longueur ou la longueur au carré, nous pouvons toujours déterminer le vecteur le plus court, sans effectuer l'opération de la racine carrée !

Cela fonctionne également pour les vecteurs plus courts que 1 : 

$$
0.1^2 = 0.01
$$

$$
0.2^2 = 0.04
$$

Donc : 

$$
0.1 < 0.2
$$

$$
0.01 < 0.04
$$
