# MAYA

## Modeling

### 01

- Menu Set에서 Shelf에 노출시킬 Menu를 Ctrl + Shift + Mouse Left

### 02

- Ctrl + Alt + Mouse Drag : Drag 방향에 따라 확대 혹은 축소

### 05

- F8 : 이전 모드와 Object 모드 전환
- F9 : Vertex 모드
- F10 : Edge 모드
- F11 : Face 모드

### 07

- z : Undo
- Z (Shift + z) : Redo

### 08

- D (Insert) : Change the pivot point
- x c v : Snap

### 11

- Edit → Delete by Type → History (Alt + Shift + D)

### 13

Create → Type

### 14

- f / Shift + f / a / Shift + a
- Edit Mesh → Merge
- Mesh Tools → Append to Polygon : Edge 선택해서 Face로 메꿈

### 15

- Create Polygon
- Multi-Cut
- Combine
- Mirror
- Smooth

### 16

- Curve Tool

### 17

- Curve → Revolve
- Curve → Reverse Direction

### 20

- Surfaces → Extrude
- Mesh Display → Reverse
- Modify → Convert → NURBS to Polygons (Tessellation method : Control points)

### 21

- Hull
- Mesh → Fill Hole

### 22

- Surfaces → Loft

### 23

- Isoparm(Mouse Right) → Curves(Menu Set) → Duplicate Surface Curves : 면에서 선을 뽑아주는 기능

### 24

- Curves(Menu Set) → Attach / Detach : 여러 커브를 합치거나 분리 (커브의 방향 주의)
- Curves(Menu Set) → Open/Close
- Surfaces(Menu Set) → Insert Isoparms

### 25

- Display → Layers → Create Layer from Selected

### 26

- Ctrl + 1 : Show → Isolate Select → View Selected

커브에 포인트 추가

1. Curve Point (Mouse Right Menu)
1. Curves (Menu Set) → Inset Knot

커브 연장

1. Curves → Add Points Tool

- Curves → Rebuild (Option : Number of spans) : 커브의 포인트를 늘이거나 줄임

```text
분리의 기준이 될 Edge 선택 후 분리
1. Edit Mesh → Detach : 분리의 기준이 될 Edge 선택 후 분리
2. Mesh → Separate
```

- Multi-Cut → Slice Tool → Extract Faces : 마우스 드레그로 폴리곤을 절단

### 27

- Multi-Cut → Ctrl + Mouse Left : 폴리곤에 한 바퀴 돌아가 있는 엣지 추가

### 28

- FX → nCloth → Create Passive Collider / Create nCloth

### 29

- Mesh → Reduce : 원하는 형태를 얻을 수 없음
- Ctrl + Del : Edit Mesh → Delete Edge/Vertex

### 31

- b → b + Mouse Middle
- nConstraint → Transform Constraint
- s : 키프레임 생성 후 적용
- nCloth1(Outliner) → Attribute Editor → nClothShape1 → Collisions → Thickness → Self Collision Flag → Full Surface

### 32

- Modify → Align Tool
- Modify → Snap Align Objects → Align Objects (Option에서 설정)

### 34

- Isoparm(Mouse Right) → Sufaces(Menu Set) → Insert Isoparms

### 35

- p / Shift p : Edit(Menu Set) → Parent / Unparent

### 37

Outliner → Display → DAG Object Only

### 41

Modify(Menu Set) → Freeze Transformations : 형태는 유지하면서 트렌스폼 값을 초기화

### 42

원하는 INPUTS 삭제

- Attribute Editor(Ctrl + a) → Select → Delete(Key)
- Windows(Menu Set) → General Editors → Hypergraph: Hierarchy → Input and output connections

## Mapping

### 44

- Windows(Menu Set) → Rendering Editors → Hypershade

### 50

- Deform → Nonlinear → Bend
- Surface Shader → Out Color → File1 → place2dTexture1

### 51

- Edit Mesh → Detach
- Mesh → Separate
- UV → UV Editor

```text
UV Editor
- Modify → Normalize
- Modify → Rotate
```

### 52

```text
UV Editor
- Image → UV Snapshot...
- Cut/Sew → Cut
```

### 53

- Mouse Right → Paint → 3D Paint

```text
3D Paint Tool
- Brush Size : b + Mouse Left Drag
- File Textures → Save Textures
```

- UV → Automatic : 겹친 UV 해결

### 54

- UV → Planer : 원하는 축으로 평면의 UV 펼침 (키보드 맵핑)

### 56

- Edit Mesh → Add Divisions : 선택한 Face에 Subdivision 추가
- Sculpting → Lift a surface (b + Left Mouse Drag : 브러시 사이즈 조정, m + Left Mouse Drag : 브러시 깊이 조정, Ctrl + Left Mouse Drag : 표면을 밀어 넣음, Shift + Left Mouse Drag : 면을 부드럽게 해줌)

### 58

- UV → Planar → (Option) Project from : 평평한 오브젝트의 UV를 펼칠때 사용

```text
UV Automatic을 크기에 비례하도록
1. Modify(Menu Set) → Freeze Transformations : 형태는 유지하면서 트렌스폼 값을 초기화
2. UV → Automatic
```

- UV로 적용된 파일의 place2dTecture에서 Repeat UV 수치를 조정하여 UV의 사이즈와 반복 조정 (Mirror U, Mirror v를 체크하여 이미지 연결부위 대칭으로 맞춰줌)

### 59

- Maya Texture의 Grid 같은 파일이 UV로 적용된다면 place2dTecture에서 Stagger를 체크하면 어긋난 페턴을 얻을 수 있음

## Light

### 61

- Ambient Light : 멀리 있는 태양을 표현 (구석이 너무 어두워 최소한의 빛을 주고자 할때 : Ambient Light → 낮은 Intensity, 낮은 Ambient Shade)
- Point Light → (Option) Decay Rate : 거리에 따른 감쇠
- Spot Light → (Option) Penumbra Angle : 경계를 뭉게줌
- Spot Light → (Option) Dropoff : 중심에서 경계까지 밝기를 조정

- (Option) Emit Diffuse : 가시광선이 없어져서 오브젝트의 색이 표현이 안됨

### 62

- Render Settings → Maya Software → Raytracing Quality → Raytracing 체크

Ambient Light

- Ambient Light에 그림자 주기 : Ambient Light → Raytrace Shadow Attributes → Use Ray Trace Shadows
- Ambient Light → Raytrace Shadow Attributes → Shadow Radius
- Ambient Light → Raytrace Shadow Attributes → Shadow Rays
- Ambient Light → Raytrace Shadow Attributes → Ray Depth Limit : 그림자를 계산하는 횟수

Ambient Light를 제외한 Light

- Depth Map Shadows : 이미지를 이용해서 간단하게 그림자를 만들어 줌, 정확도는 떨어지고 속도는 빠름
- Raytrace Shadow Attributes → Light Angle
- Raytrace Shadow Attributes → Shadow Rays

### 63

- windows → Settings/Preferences → Plug-in Manager → (search) mtoa.mll : Arnold 활성화

### 67

- Render Settings → Arnold Renderer → (Option) Camera (AA) : 노이즈가 있을 경우 이 값을 올려줌
- Rendering (Switch Menu Set) → Render (Menu Set) → Render Sequence (Arnold) / Batch Render (Maya Software, Arnold는 라이센스 문제로 불가능)
- Camera → Attribute Editor → Output Settings → (Option) Renderable

### 68

- 3D Texture가 적용된 오브젝트를 Material과 오브젝트를 같이 선택하고 Hypershade → Edit → Convert to File Tecture : 이미지 Texture로 적용

### 70

- UV Editor → Tools → Lattice : UV 격자 변경
- Mesh → Transfer Attributes → (Option) UV Sets-Current, Sample space-Component : 동일 오브젝트들에서 가공된 UV를 다른 오브젝트에 적용

### 74

UV 조절

- UV → Planar → (Option) Keep image width/height ratio

1. UV Editor → Cut/Sew → Cut
1. UV Editor → Cut/Sew → Move and Sew

- UV Editor → UV Toolkit → Transform → Texel Density : UV 비율 맞추기

### 76

투명한 오브젝트 굴절

- blinn → Raytrace Options → Refractions
- blinn → Raytrace Options → Refractive Index (오브젝트에 맞는 굴절률 적용)
- blinn → Raytrace Options → Refraction Limit (굴절 횟수)

- aiStandardDurface → IOR (굴절률)
