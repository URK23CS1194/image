 4 – Tamil Nadu Tourist Places Gallery

## Step 1: Open your project

1. Open VS Code.
2. Click File → Open Folder.
3. Select `C:\Users\sujan\Downloads\flut4`.
4. Click Select Folder.
5. You should see your Flutter project on the left Explorer panel.

## Step 2: Create the image folders

In the Explorer panel:

1. Right-click `flut4`.
2. Select New Folder.
3. Type `assets`.
4. Right-click `assets`.
5. Select New Folder.
6. Type `images`.

You should now have:

```
flut4
 ├── assets
 │    └── images
 ├── lib
 │    └── main.dart
 └── pubspec.yaml
```

## Step 3: Download the three images

Open Google Chrome.

Search and download:

- Ooty tourist place image.
- Kodaikanal tourist place image.
- Kanyakumari tourist place image.

Save all three images inside:

`flut4/assets/images/`

Rename them exactly:

```
ooty.jpg
kodaikanal.jpg
kanyakumari.jpg
```

## Step 4: Configure pubspec.yaml

1. Go back to VS Code.
2. Click `pubspec.yaml`.
3. Find the `flutter:` section near the bottom.
4. Make it look like this:

```
flutter:
  uses-material-design: true

  assets:
    - assets/images/
```

5\. Press `Ctrl + S`.

## Step 5: Install the assets

Open the VS Code terminal.

Click:

Terminal → New Terminal

Make sure the terminal path is:

```
PS C:\Users\sujan\Downloads\flut4>
```

Type:

```
flutter pub get
```

Press Enter.

Wait until you see:

```
Got dependencies!


## Step 6: Write the Flutter program

1. On the left side, open `lib`.
2. Click `main.dart`.
3. Select all existing code using `Ctrl + A`.
4. Delete it.
5. Paste the following code.

```


import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: GalleryPage(),
    );
  }
}

class GalleryPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.grey[100],

      appBar: AppBar(
        title: Text("Tamil Nadu Tourism Gallery"),
        backgroundColor: Colors.green[800],
        foregroundColor: Colors.white,
        centerTitle: true,
      ),

      body: Padding(
        padding: EdgeInsets.all(12),

        child: GridView.count(
          crossAxisCount: 2,
          crossAxisSpacing: 12,
          mainAxisSpacing: 12,
          childAspectRatio: 0.85,

          children: [

            touristCard("Ooty", "assets/images/ooty.jpg"),

            touristCard("Kodaikanal", "assets/images/kodaikanal.jpg"),

            touristCard("Kanyakumari", "assets/images/kanyakumari.jpg"),

          ],
        ),
      ),
    );
  }

  Widget touristCard(String name, String image) {
    return Card(
      elevation: 4,
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(15),
      ),

      child: Column(
        children: [

          Expanded(
            child: ClipRRect(
              borderRadius: BorderRadius.vertical(
                top: Radius.circular(15),
              ),

              child: Image.asset(
                image,
                width: double.infinity,
                fit: BoxFit.cover,
              ),
            ),
          ),

          Padding(
            padding: EdgeInsets.all(12),
            child: Text(
              name,
              style: TextStyle(
                fontSize: 18,
                fontWeight: FontWeight.bold,
              ),
            ),
          ),

        ],
      ),
    );
  }
}

```

6\. Press `Ctrl + S` to save.

## Step 7: Run the application

In the terminal, type:

```
flutter run
```

If you want to run it in Google Chrome instead:

```
flutter run -d chrome
```

Wait for Flutter to build and launch the application.

## Step 8: Check your final output

You should see:

Tamil Nadu Tourism Gallery

[Tea Garden Ooty - PankajSinghPhotographie](https://images.openai.com/static-rsc-4/tLFeqORGsf56-Un-KK3eyoryOgcIlEo4_SKzld4go-SFCsjg8iCJAuByYZMe8jl133MFx_u44uQObTP6oN-3TV_GpvTe5J37APwT-r8WWpK_pQ8US219N7BwfB4a2Mpk2TFKbWHerzF0GsGBr5S1ErI-d2Rh5s1d_bPTwiXJwJ0?purpose=inline)

Ooty

[Kodaikanal Lake (Princess of Hill stations), Tamil Nadu, India](https://images.openai.com/static-rsc-4/-39sBf-TrDRDrg8Tm0KO1T4nWn6uNJow65tBL5zVRpVmU1Zx2qnoE8v3IGdxoCvRaGakUoZi23KghnS7HlSxaUdi0EIvozBHMVvadHzS2EUtjtmmuVDWfVr1R_JcezG3hWGrnOqvfYDQIZAr6A-0pX7xdiiPJSd_V5ePi6qa9FU95fi1ADyYF_Zm9sjNETcn?purpose=inline)

Kodaikanal

[2 Nights 3 Days Kanyakumari Tour Package - Myholidays.com](https://images.openai.com/static-rsc-4/zADRLXx05vjrcwvrrjZkHeAYhODF9yWMg-CD9zayLD7RdWcjsIQWh45QBLzzeWYhH5BAPaheTPiz8T6afE1plflPiLVULjZiMNjKWbXzdWFydYEO8CY_gKsfsdQ3thfK9BsFWInLgKgqgMPJ2tf52ucqJR6fb7BTjdesctEVfpo?purpose=inline)

Kanyakumari

## Your practical exam memory trick

Remember this order:

1. Create project
2. Create assets/images folders
3. Add three photographs
4. Configure pubspec.yaml
5. Run flutter pub get
6. Write main.dart code
7. Run flutter run
8. Check output

Let's do it one step at a time: Since `flutter pub get` is already successful, your next task is to add the three photographs into `assets/images`. Then we can run your application.
