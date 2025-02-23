---
title: People detection - Computer Vision
titleSuffix: Azure Cognitive Services
description: Learn concepts related to the people detection feature of the Computer Vision API - usage and limits.
services: cognitive-services
author: PatrickFarley
manager: nitinme

ms.service: cognitive-services
ms.subservice: computer-vision
ms.custom: ignite-2022
ms.topic: conceptual
ms.date: 09/12/2022
ms.author: pafarley
---

# People detection (preview)

Version 4.0 of Image Analysis offers the ability to detect people appearing in images. The bounding box coordinates of each detected person are returned, along with a confidence score. 

> [!IMPORTANT]
> you need Image Analysis version 4.0 to use this feature. Version 4.0 is currently available to resources in the following Azure regions: East US, France Central, Korea Central, North Europe, Southeast Asia, West Europe, West US.

## People detection example

The following JSON response illustrates what the Analyze API returns when describing the example image based on its visual features.

![Photo of a woman in a kitchen.](./Images/windows-kitchen.jpg).

```json
{
    "metadata":
    {
        "width": 1260,
        "height": 473
    },
    "peopleResult":
    {
        "values":
        [
            {
                "boundingBox":
                {
                    "x": 660,
                    "y": 0,
                    "w": 582,
                    "h": 473
                },
                "confidence": 0.9680353999137878
            }
        ]
    }
}
```

## Use the API

The people detection feature is part of the [Analyze Image](https://aka.ms/vision-4-0-ref) API. You can call this API using REST. Include `People` in the **visualFeatures** query parameter. Then, when you get the full JSON response, parse the string for the contents of the `"people"` section.

## Next steps

Learn the related concept of [Face detection](concept-face-detection.md).
