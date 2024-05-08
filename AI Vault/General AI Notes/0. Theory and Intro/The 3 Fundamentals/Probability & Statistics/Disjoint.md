Disjoint is a concept from probability and statistics. The idea behind disjoint is that two or more events _do not_ overlap at all. 

For example: A dice roll can be any number 1-6, but you could never get __1 AND 6__ ($1 \bigcap 6$). These two events are disjoint because they never appear at the same time.

![Disjoint events|600](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimage1.slideserve.com%2F2595190%2Fdisjoint-events-l.jpg&f=1&nofb=1&ipt=cc1438ba7dd8bac91c1a6203d6cb5b243979890a6917646726b3c1dfc39758ed&ipo=images)


## Machine Learning Applications
Disjoint can apply to problems that seemingly do not fit within probability and statistics. For the Wok Robot Project, the [[IOU - Intersection Over Union|Intersection Over Union]] was used to calculate the overlap of 2 point shapes. Each of these shapes represented positions. We wanted to use the IOU as a loss function since we wanted to maximize the overlap of the two shapes. The problem is - if the two shapes are _disjoint_ (i.e. their paths never overlap), we cannot extract any information about how to _get them to overlap_ from using only the IOU.