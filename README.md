### 👋

I'm Robbie, a developer and undergraduate (penultimate year) at the University of Edinburgh.
Game engine development and real-time graphics are fundamentally very important to me, I spend a lot of my time furthering my understanding of game engines via practical applications and getting myself up to speed with real-time rendering research.

Thoughts on my recent progress:
\
I've just finished looking at the specular occlusion technique GTSO described in the Jimenez et al. (Activision) 2016 GTAO paper, and implemented a similar version in my game engine. This version uses the adjacent cone-cone approximation described at the end of the paper, different from the cone-lobe approximation which is more physically accurate but requires precomputation. My implementation also uses SSAO bent normals input, different from the GTAO input in the paper. After testing and investigation of artefacts, I found that the small bent normal artifacts caused by SSAO sampling and self-occlusion contribute massively to the resultant specular occlusion term at grazing light angles. My temporary conclusion is that the specular cone being allowed to leak past the visible hemisphere in the SO term outlined by the paper allows small visibility artefacts to massively impact occlusion at grazing angles. I modified the term to treat the specular cone solid angle as the area of intersection between the cone and the perfect visibility hemisphere, resulting in a large increase in visual fidelity.

\
Most of my repositories are relatively old, so please keep that in mind


west.a.robbie@gmail.com, R.West-6@sms.ed.ac.uk
