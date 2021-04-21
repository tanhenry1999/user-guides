---
layout: default
title: Task Sequence
parent: SCCM1
---

## Task Sequence
{: .no_toc }

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Update Windows Image
---

## Update Application/ Package Image
---

### For Editing Application Type
---

1. Open System Center Configuration Manager

2. Browse and Expand to Software Library -> Operating Systems -> Task Sequences -> STUAFF -> ASI

3. Right Click on Task Sequences that needs to be altered, Edit

4. Scroll and select application name on the left side that needs update

5. Select Software in the box on right side middle, Click on red "X"

6. Click on the "Sun" icon next to the red X

7. Browse and expand root -> STUAFF -> ASI -> "Software folder" and select new version software on right side

8. ok, apply, ok

### For Exiting Package Type
---
1. Open System Center Configuration Manager
2. Browse and Expand to Software Library -> Operating Systems -> Task Sequences -> STUAFF -> ASI
3. Right Click on Task Sequences that needs to be altered, Edit
4. Scroll and select application name on the left side that needs update
5. Select Install a single software package
6. Browse and expand root -> STUAFF -> ASI -> "Software folder" and select new version software on right side
7. ok, apply, ok

## Exporting Image Task Sequence for USB Key
---
1. Open System Center Configuration Manager
2. Browse and Expand to Software Library -> Operating Systems -> Task Sequences -> STUAFF -> ASI
3. Click "Create Task Sequence media" located top left
4. Stand-alone media, next
5. change cd/dvd set media size to "unlimited"
6. Media File: Browse to \\Server\SCCM\Boot Images
7. Give name using the task sequence that is expected to be exported (e.g export TS AS-WIN10x64-BitLocker-052516, or AS-WIN10x64-fw-052516)
8. Save, Next,
9 uncheck protected media with a password, next
10. browse and expand to root -> STUAFF -> ASI ->
11. Select Task Sequence that is going to be used
12. Next, Add all distribution points, next
