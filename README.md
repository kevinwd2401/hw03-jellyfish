# Procedural Jellyfish


This procedural jellyfish was made in Houdini, comprised of a bell, veins, organs, arms, and tentacles.



https://github.com/user-attachments/assets/e06a44ac-4128-49de-8068-009d00626066




https://github.com/user-attachments/assets/485942f7-8e63-4574-9c6a-83388065cdac



---

## Bell

By creating a line, bending it, and revolving it around the y-axis, we create a bell shape that we can then animate by modifying the bending angles and y-position.


<img width="1195" height="808" alt="image" src="https://github.com/user-attachments/assets/8049151b-f0b6-44e1-94de-36d8347eff9c" />

---

## Arms

The arms are created from a long rectangular grid, and its side edges are displaced by sin waves and noise to create ribbon shapes. It is then twisted, duplicated, and then a Vellum cloth simulation is applied, with the top pinned in place, deforming with the animation of the bell.


<img width="1136" height="995" alt="image" src="https://github.com/user-attachments/assets/a1aa205c-103d-4894-9fbd-e485d7054398" />

---

## Veins

The bell is remeshed into triangles, and then random points on the top and bottom portions of the bell are chosen. The veins are created through the shortest path node, in which we connect each bottom point with the nearest top point, creating a veiny structure. The points are merged with the fuse node and the curve is smoothed to create a more natural look. The curves are then given thickness, and it is deformed to follow the surface of the bell.


<img width="1194" height="876" alt="image" src="https://github.com/user-attachments/assets/dab7a146-8258-4286-aa8a-e2c7550cf15b" />

---

## Organs

Starting with circle geometry, we get the edges, delete a portion, and then extrude the remaining edges with the sweep node. It is then remeshed before being deformed with noise through the mountain node.


<img width="1127" height="847" alt="image" src="https://github.com/user-attachments/assets/d9b26f3d-a7d1-4405-9954-7207daf51560" />

---

## Tentacles

We get points distributed across the bottom of the bell with the scatter node, and then copy lines to these points. The scale of the points have been modified by the attribute randomize node, giving the tentacles different lengths. We then apply a Vellum hair simulation similar to the arms, with lots of drag and low gravity force.


<img width="1139" height="909" alt="image" src="https://github.com/user-attachments/assets/0498fdf4-960f-4921-92d8-3cf1353be028" />
