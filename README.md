void main() {
  var borsh = Recipe();
  
  var kapusta = Component();
  kapusta.name = "Капуста";
  kapusta.count = 300;
  var kartoshka = Component();
  kartoshka.name = "Картошка";
  kartoshka.count = 200;
  var svekla = Component();
  svekla.name = "Свёкла";
  svekla.count = 100;
  borsh.add(kapusta);
  borsh.add(kartoshka);
  borsh.add(svekla);
  borsh.printComponents();
}
class Component {
  String name = "";
  int count = 0;
}
void printList(List list) {
  for (int i = 0; i < list.length; i = i + 1) {
    (print (list[i].name + " " + list[i].count.toString()));
  }
}

class Recipe {
  List components = [];

  void add(Component component) {
    components.add(component);
  }

  void printComponents() {
    printList(components);
  }

  num componentsCounts() {
    return components.length;
  }
}
