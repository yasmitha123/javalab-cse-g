## Tittle : miniproject
```
import java.util.ArrayList;
import java.util.Scanner;

class Product {
    private int id;
    private String name;
    private double price;

    public Product(int id, String name, double price) {
        this.id = id;
        this.name = name;
        this.price = price;
    }

    public int getId() { return id; }
    public String getName() { return name; }
    public double getPrice() { return price; }

    @Override
    public String toString() {
        return id + " | " + name + " | " + price;
    }
}

public class EcommerceCart {

    static ArrayList<Product> products = new ArrayList<>();
    static ArrayList<Product> cart = new ArrayList<>();

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Predefined products
        products.add(new Product(1, "Laptop", 50000));
        products.add(new Product(2, "Mobile", 20000));
        products.add(new Product(3, "Shoes", 2000));
        products.add(new Product(4, "Watch", 3000));

        while(true) {
            System.out.println("\n===== MINI E-COMMERCE CART =====");
            System.out.println("1. View Products");
            System.out.println("2. Add to Cart");
            System.out.println("3. View Cart");
            System.out.println("4. Calculate Total");
            System.out.println("5. Remove Item");
            System.out.println("6. Exit");
            System.out.print("Choose option: ");

            int choice = sc.nextInt();

            switch(choice) {
                case 1: viewProducts(); break;
                case 2: addToCart(sc); break;
                case 3: viewCart(); break;
                case 4: calculateTotal(); break;
                case 5: removeItem(sc); break;
                case 6:
                    System.out.println("Thank you for shopping!");
                    System.exit(0);
                default:
                    System.out.println("Invalid choice!");
            }
        }
    }

    public static void viewProducts() {
        System.out.println("\nAvailable Products:");
        for(Product p : products) {
            System.out.println(p);
        }
    }

    public static void addToCart(Scanner sc) {
        System.out.print("Enter Product ID: ");
        int id = sc.nextInt();

        boolean found = false;

      for(Product p : products) {
            if(p.getId() == id) {
                cart.add(p);
                System.out.println("Product added to cart!");
                found = true;
                break;
            }
        }

        if(!found) {
            System.out.println("Invalid Product ID!");
        }
    }

    public static void viewCart() {
        if(cart.isEmpty()) {
            System.out.println("Cart is empty.");
        } else {
            System.out.println("\nItems in Cart:");
            for(Product p : cart) {
                System.out.println(p.getName() + " | " + p.getPrice());
            }
        }
    }

    public static void calculateTotal() {
        double total = 0;
        for(Product p : cart) {
            total += p.getPrice();
        }
        System.out.println("Total Amount: " + total);
    }

    public static void removeItem(Scanner sc) {
        System.out.print("Enter Product ID to remove: ");
        int id = sc.nextInt();

        boolean removed = false;

        for(Product p : cart) {
            if(p.getId() == id) {
                cart.remove(p);
                System.out.println("Item removed from cart.");
                removed = true;
                break;
            }
        }

        if(!removed) {
            System.out.println("Item not found in cart.");
        }
    }
}
```
# output
![output of miniproject](mini1.png)
