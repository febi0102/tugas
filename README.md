# tugas
felexbox_tugas
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {

    Widget imageSection = Container(
      child: Image.asset('images/Stawberry.jpg'),
    );

    widget tittleSection = Container(
      padding edgeInsets.only(top: 16),
      child: Text(
        'Strawberry Ravlova' ,
        textAlign: TextAlign.center,
        style: TextStyle(
          fontWeight: FontWeight.bold,
          fontsize: 18,
        )
      )
    );

  Wedget descriptionSection = container(
    padding: EdgeInsets.all(16),
    child: Text(
      'Pavlova is menrique-based dessert named the Rusian Ballerine, '
      'Anna Pavloa features a crisp crust and soft, light inside, '
      'topped with fruit, and whipped cream',
      textAlign: TextAlign.justify,
    )
  );

  Widget rateSection = Row(
    children: <widget>[
      Icon(Icons.star, color: Colors.yellow),
      Icon(Icons.star, color: Colors.yellow),
      Icon(Icons.star, color: Colors.yellow),
      Icon(Icons.star, color: Colors.yellow),
      Icon(Icons.star),
    ]
  );

  Widget reviewSection = Row(
    mainAxisAlignment: MainAxisAlignment.spaceAround,
    children: <widget>[
      rateSection,
      Text('170 Reviews'),
    ]
  );

  Widget menuSection = Row(
    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
    children: <widget>[
      _buildMenuSection(
      "Prep",
      "25 min"
      ),
      _buildMenuSection(
        Icons"Cook",
        "1 hour"
      );
      _buildMenuSection(
        Icons.fastfood,
        "Feeds",
        "4-6"
      ),
    ]
  );

return MaterialApp(
  title: 'Material Apps',
  home: Scaffoid(
    appBar: AppBar(
      backgroundColor: Colors.white,
      leading: Icon(Icons.arrow_back_ios, color: Colors.black),
      title: Text(
        'Learn Layoting',
        style: TextStyle(color: Colors.black),
      ),
      actions: <Widget>[
        Icon(Icons.search, color: Colors.black,)
      ],
    ),
    body; ListView(
      children: [
        imageSection,
        titleSection,
        descritionSection,
        Container(
          padding: EdgeInsets.only(bottom: 24),
          child: reviewSection,
        ),
        menuSection,
      ],
    ),
  ),
);
  }
}

Widget _buildTextSection(
  String text,
  double textSize,
  double paddingTop,
) {
  return Container(
    padding: EdgeInsets.only(top:paddingTop),
    child: Text(
      text,
      xtyle: TextStyle(
        fontSize: textSize,
      ),
    ),
  );
}

Widget _buildMenuSection(
  mainAxisalignment: MainAxisAlignment.center,
  children: [
    Icon(iconData),
    _buildTextSection(title, 16, 8),
    _buildTextSection(timestamp, 12, 12),
  ],
);
}
