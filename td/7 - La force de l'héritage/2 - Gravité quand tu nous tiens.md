---
goal:Une première implémentation pour notre interface
notions:Héritage, polymorphisme
---
Écrivez une classe `Gravity` qui implémente la méthode `Force::get` et retourne une force constante `Point2D(0, -9.81)`

Vérifiez que la classe fait passer le test suivant :

    TEST(Gravity, Check) {
        Gravity gravity;
        EXPECT_EQ(gravity.get(Point2D(), 0), Point2D(0, -9.81));
        // position et temps n'influent pas la force
        EXPECT_EQ(gravity.get(Point2D(1,2), 3), Point2D(0, -9.81));
    }
