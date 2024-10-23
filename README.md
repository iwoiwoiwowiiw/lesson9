public class Practicum {

    public static void main(String[] args) {
        Cat cat = new Cat();
        cat.catchMouse();
        cat.giveVoice();

        Dog dog = new Dog();
        dog.bringStick();
        dog.play();

        Hamster hamster = new Hamster();
        hamster.hideFood();
        hamster.sleep();

        Fish fish = new Fish();
        fish.sleep();

        Spider spider = new Spider();
        System.out.println("У паука " + spider.getPawsCount() + " лапок.");
    }

}

abstract class Pet {

    private String voice;
    private int pawsCount;

    protected Pet(int pawsCount) {
        this.pawsCount = pawsCount;
    }

    //public Pet(String voice, int pawsCount) {
        //this.voice = voice;
        //this.pawsCount = pawsCount;
    //}

    public void sleep(){
        System.out.println("sleeping");
    }

    public void play(){
        System.out.println("playing");
    }

    public int getPawsCount(){
        return pawsCount;
    }

    public void giveVoice() {
        System.out.println(voice);
    }
}

class Fish extends Pet {

    public Fish() {
        super(4);
    }

    @Override
    public void giveVoice() {
        System.out.println("...");
    }

    public void eatSeaweed() {
        System.out.println("ate seaweed");
    }

}

class Spider extends Pet {

    public Spider() {
        super(8);
    }

    @Override
    public void giveVoice() {
        System.out.println("ch-ch");
    }

    public void weavesWeb() {
        System.out.println("weaves a web");
    }

}

class Dog extends Pet {

    public Dog() {
        super(4);
    }

    @Override
    public void giveVoice() {
        System.out.println("Woof-Woof");
    }

    public void bringStick() {
        System.out.println("he brought his wand like a good boy!");
    }

}

class Cat extends Pet {

    public Cat() {
        super(4);
    }

    @Override
    public void giveVoice() {
        System.out.println("Meow");
    }

    public void catchMouse() {
        System.out.println("caught a mouse");
    }

}

class Hamster extends Pet {

    public Hamster() {
        super(4);
    }

    @Override
    public void giveVoice() {
        System.out.println("pi-pi-pi");
    }

    public void hideFood() {
        System.out.println("all kinds of food in the cheeks");
    }

}
