---
title: "Nvidia GPUs just got a huge upgrade, and no one is talking about it"
publication: "Digital Trends"
pubDate: 2025-11-03
url: "https://www.digitaltrends.com/computing/new-nvidia-tech-brings-performance-improvements/"
---

# Nvidia GPUs just got a huge upgrade, and no one is talking about it
Alan Wake 2 has released its 1.2.8 update, making it one of the first games to use Nvidia’s new RTX Mega Geometry tech. In a comparison video released by [Compusemble](https://www.youtube.com/watch?v=_lxg6TRvn70&t=195s) and reported on by [Wccftech](https://wccftech.com/alan-wake-2-rtx-mega-geometry-performance-vram-improvements/), the results appear to be an average 13% reduction in VRAM usage and an fps bump — and that’s while using an RTX 4090. 

The video runs the 1.2.7 version of the game and the 1.2.8 update side by side, with one comparison using DLAA and the next using DLSS. The game is running on an [RTX 4090 graphics card](https://www.digitaltrends.com/computing/nvidia-geforce-rtx-4090-review/) at 4K resolution with settings set to max. If you keep an eye on the numbers, you can easily spot the lower CPU percentages and the higher frame rates.

Although Mega Geometry was introduced alongside the new RTX 50-series as part of the Nvidia RTX kit, this tech runs on all RTX GPUs and according to this example, it can bring significant improvements even to older models. The recently released RTX 5090 and 5080 GPUs include fourth-generation ray tracing cores that were built to work with Mega Geometry, so the results there will likely be even more impressive.

## What is RTX Mega Geometry?
You may not have heard much about RTX Mega Geometry but it is a huge deal for performance and quality in ray-traced games because it both increases the number of triangles developers can ray-trace and reduces the CPU overhead required to pull it off. How does it do this? With artificial intelligence, of course!

One of the most expensive aspects of ray tracing is connected to the different LODs (level of detail) each game object has. When an object is closest to the camera, we see a high-detail mesh with lots of tiny triangles, typically referred to as LOD 0. As the LOD level goes up, we get less detail and fewer triangles, which is suitable for objects that are far away from the camera. 

As you move around, the LODs for different objects are constantly changing based on how far away they are from the camera. The more triangles you’re working with overall, the more levels of detail are possible — which means more LODs to swap between. 

This has been standard practice for a long time, but now that we’re dealing with newer tech like ray tracing and Nanite, things have been getting out of hand. Unreal 5’s Nanite system allows for a huge increase in geometry complexity — meaning more triangles and more levels of detail. In a game using Nanite, there could be hundreds or even thousands of LOD changes in every single frame.

The problem with this is that in a ray-traced game, every time one LOD is swapped out for another, a whole rebuild has to happen to apply ray tracing to the new mesh. This is incredibly expensive to do and if you end up with too many LOD changes, it can become impossible to achieve real-time frame rates. 

To fix this, RTX Mega Geometry updates clusters of triangles in batches, intelligently choosing which to update and when for optimal efficiency. The goal is to enable developers using Nanite to ray trace every triangle in their projects while still achieving acceptable real-time frame rates. The implication of all this? More ray tracing and better performance for everyone! Well, right now it’s only for Nvidia RTX users, but this tech will definitely spread across the industry over time.

The addition of RTX Mega Geometry to Alan Wake 2 is automatic when you update the game, so you can easily try it out for yourself if you use an Nvidia RTX GPU. 