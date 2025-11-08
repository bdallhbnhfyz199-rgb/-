# -import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(Profile());
}

class Profile extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      // إزالة شارة DEBUG
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        // خلفية فاتحة
        backgroundColor: Colors.teal[50],
        appBar: AppBar(
          backgroundColor: Color(0xFF004D40), // لون أخضر غامق
          title: Text('الملف الشخصي', style: TextStyle(color: Colors.white)),
        ),
        body: Column(
          children: [
            // قسم الرأس: الصورة والاسم
            Container(
              width: double.infinity,
              color: Color(0xFF00695C),
              child: Column(
                mainAxisAlignment: MainAxisAlignment.center,
                children: [
                  SizedBox(height: 17),
                  // الصورة الشخصية (يجب توفير ملف الصورة في مجلد assets/images)
                  CircleAvatar(
                    radius: 81,
                    backgroundColor: Colors.white,
                    child: CircleAvatar(
                      radius: 80,
                      backgroundImage: Image.asset(
                        'images/abdullah_profile.png', // تم تعديل مسار الصورة
                      ).image,
                    ),
                  ),
                  SizedBox(height: 22),
                  // الاسم
                  Text(
                    'عبد الله بن سالم بن حفيظ بن الشيخ ابوبكر', // الاسم الجديد
                    textAlign: TextAlign.center,
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 24, // زيادة الحجم ليتناسب مع طول الاسم
                      fontFamily: 'Pacifico',
                    ),
                  ),
                  Divider(color: Colors.white),
                  // المسمى الوظيفي
                  Text(
                    'منسق فني في قسم ابحاث خاص يمؤسسه', // المسمى الوظيفي الجديد
                    textAlign: TextAlign.center,
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 22,
                      fontFamily: 'Pacifico',
                    ),
                  ),
                  SizedBox(height: 17),
                ],
              ),
            ),
            
            // قسم التواصل: البريد الإلكتروني
            Container(
              alignment: Alignment.center,
              padding: EdgeInsets.symmetric(horizontal: 20),
              width: double.infinity,
              height: 80,
              color: Color(0xFF00796B),
              child: Row(
                mainAxisAlignment: MainAxisAlignment.spaceBetween,
                children: [
                  Text('البريد الإلكتروني',
                      style: TextStyle(fontSize: 20, color: Colors.white)),
                  Text('abdullah.shafee@research.com', // البريد الإلكتروني الجديد
                      style: TextStyle(fontSize: 18, color: Colors.white))
                ],
              ),
            ),
            
            // قسم التواصل: الهاتف
            Container(
              alignment: Alignment.center,
              padding: EdgeInsets.symmetric(horizontal: 20),
              width: double.infinity,
              height: 80,
              color: Color(0xFF00897B),
              child: Row(
                mainAxisAlignment: MainAxisAlignment.spaceBetween,
                children: [
                  Text('الهاتف',
                      style: TextStyle(fontSize: 22, color: Colors.white)),
                  Text('738567482', // رقم الهاتف الجديد
                      style: TextStyle(fontSize: 22, color: Colors.white))
                ],
              ),
            ),
            
            // قسم المهارات
            Container(
              width: double.infinity,
              height: 285,
              color: Color(0xFF009688),
              padding: EdgeInsets.all(15),
              child: Column(
                children: [
                  Text('المهارات',
                      style: TextStyle(fontSize: 22, color: Colors.white, fontWeight: FontWeight.bold)),
                  Divider(color: Colors.white),
                  Row(
                    children: [
                      Spacer(),
                      // العمود الأول: المهارات العلمية
                      Column(
                        crossAxisAlignment: CrossAxisAlignment.start,
                        children: [
                          Text('المهارات العلمية:',
                              style:
                                  TextStyle(fontSize: 20, color: Colors.white, decoration: TextDecoration.underline)),
                          SizedBox(height: 10),
                          Text('1- تصميم تنسيق',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                          Text('2- التخطيط الاستراتيجي',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                          Text('3- تحليل البيانات',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                          Text('4- إدارة المشاريع',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                          Text('5- كتابة التقارير الفنية',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                        ],
                      ),
                      Spacer(),
                      // العمود الثاني: المهارات المهنية
                      Column(
                        crossAxisAlignment: CrossAxisAlignment.start,
                        children: [
                          Text('المهارات المهنية:',
                              style:
                                  TextStyle(fontSize: 20, color: Colors.white, decoration: TextDecoration.underline)),
                          SizedBox(height: 10),
                          Text('1- Flutter/Dart',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                          Text('2- API Integration',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                          Text('3- State Management',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                          Text('4- Git/GitHub',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                          Text('5- Mobile Testing',
                              style: TextStyle(fontSize: 18, color: Colors.white)),
                        ],
                      ),
                      Spacer()
                    ],
                  )
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
