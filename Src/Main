import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        ContactBook contactBook = new ContactBook();

        while (true) {
            System.out.println("\n1. Добавить контакт");
            System.out.println("2. Удалить контакт");
            System.out.println("3. Найти контакт");
            System.out.println("4. Показать все контакты");
            System.out.println("5. Выйти");
            System.out.print("Выберите действие: ");
            int choice = scanner.nextInt();
            scanner.nextLine(); // очистка буфера

            switch (choice) {
                case 1:
                    System.out.print("Введите имя: ");
                    String name = scanner.nextLine();
                    System.out.print("Введите телефон: ");
                    String phone = scanner.nextLine();
                    System.out.print("Введите email: ");
                    String email = scanner.nextLine();
                    contactBook.addContact(new Contact(name, phone, email));
                    System.out.println("Контакт добавлен.");
                    break;
                case 2:
                    System.out.print("Введите имя контакта для удаления: ");
                    String nameToDelete = scanner.nextLine();
                    boolean deleted = contactBook.deleteContact(nameToDelete);
                    System.out.println(deleted ? "Контакт удалён." : "Контакт не найден.");
                    break;
                case 3:
                    System.out.print("Введите имя для поиска: ");
                    String nameToFind = scanner.nextLine();
                    Contact found = contactBook.findContact(nameToFind);
                    System.out.println(found != null ? found : "Контакт не найден.");
                    break;
                case 4:
                    contactBook.listContacts();
                    break;
                case 5:
                    System.out.println("Выход из программы.");
                    return;
                default:
                    System.out.println("Неверный ввод.");
            }
        }
    }
}
