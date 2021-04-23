Creating Widget
-----------------
Widget build(BuildContext context){
    return M

}


---
SizedBox(height:20), //for creating space b/w two Widget
SizedBox(width:20), //for creating space b/w two Widget
---
Divider(
height: 90,
color: Colors.green,
),

---
CircleAvator(

backgroundImage: AssetImage('assets/bg1.jpg'),
radius: 40,

),

---
//to change vairale data
setState(() {
level += 1;
}
);

---
///
body: Center(
            child: IconButton(
              onPressed: () {},
              icon: Icon(Icons.access_alarm),
              color: Colors.amber,
            ),
            // child: RaisedButton.icon(
            //   onPressed: () {},
            //   icon: Icon(
            //     Icons.book,
            //     color: Colors.white,
            //   ),
            //   label: Text(
            //     'Book',
            //     style: TextStyle(color: Colors.white),
            //   ),
            //   color: Colors.red,
            // ),
            // child: RaisedButton(
            //   onPressed: () {
            //     print('you Cliked button');
            //   },
            //   child: Text('Button 1'),
            //   color: Colors.red,
            // ),
            // child: Icon(
            //   Icons.airport_shuttle,
            //   color: Colors.amber,
            //   size: 60,
            // ),
            // child: Text(
            //   'Hello World',
            //   style: TextStyle(
            //       fontSize: 20,
            //       color: Colors.deepPurple,
            //       fontWeight: FontWeight.bold,
            //       letterSpacing: 3),
            // ),
            // child: Image(
            //     //image using assest
            //     //image: AssetImage('assets/bg1.jpg'),
            //     // image using link
            //     // image: NetworkImage(
            //     //     'https://images.unsplash.com/photo-1562813733-b31f71025d54?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8cHJvZ3JhbW1lcnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80'),
            //     ),
          ),
          
---
body: Row(
            mainAxisAlignment: MainAxisAlignment.spaceEvenly,
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
              Container(
                color: Colors.amber,
                padding: EdgeInsets.all(10),
                child: Text('hello container'),
              ),
              IconButton(
                onPressed: () {},
                icon: Icon(Icons.access_alarm),
                color: Colors.amber,
              ),
              RaisedButton.icon(
                onPressed: () {},
                icon: Icon(
                  Icons.book,
                  color: Colors.white,
                ),
                label: Text(
                  'Book',
                  style: TextStyle(color: Colors.white),
                ),
                color: Colors.red,
              ),
              RaisedButton(
                onPressed: () {
                  print('you Cliked button');
                },
                child: Text('Button 1'),
                color: Colors.red,
              ),
              Icon(
                Icons.airport_shuttle,
                color: Colors.amber,
                size: 60,
              ),
              Text(
                'Hello World',
                style: TextStyle(
                    fontSize: 20,
                    color: Colors.deepPurple,
                    fontWeight: FontWeight.bold,
                    letterSpacing: 3),
              ),
              Image(
                image: AssetImage('assets/bg1.jpg'),
              ),
            ],
          ),
          
---

body: Row(
            children: [
              Expanded(
                flex: 3,
                child: Container(
                  padding: EdgeInsets.all(10),
                  color: Colors.red,
                  child: Text('1'),
                ),
              ),
              Expanded(
                flex: 2,
                child: Container(
                  padding: EdgeInsets.all(10),
                  color: Colors.green,
                  child: Text('3'),
                ),
              ),
              Expanded(
                flex: 1,
                child: Container(
                  padding: EdgeInsets.all(10),
                  color: Colors.blue,
                  child: Text('3'),
                ),
              ),
            ],
          ),

---

// padding: EdgeInsets.fromLTRB(10, 10, 10, 10),
            // // margin: EdgeInsets.fromLTRB(10, 10, 10, 10),
