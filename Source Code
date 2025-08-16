struct medication { 
    int id; 
    char name[100]; 
    float price; 
    int quantity; 
}; 
 
struct medication meds[100]; 
int numMeds = 0; 
 
void addMedication() { 
    printf("Enter medication ID: "); 
    scanf("%d", &meds[numMeds].id); 
    printf("Enter medication name: "); 
    scanf("%s", meds[numMeds].name); 
    printf("Enter medication price: "); 
    scanf("%f", &meds[numMeds].price); 
    printf("Enter medication quantity: "); 
    scanf("%d", &meds[numMeds].quantity); 
    numMeds++; 
} 
 
void searchMedication(int id) { 
    for (int i = 0; i < numMeds; i++) { 
        if (meds[i].id == id) { 
            printf("Medication ID: %d\n", meds[i].id); 
            printf("Medication Name: %s\n", meds[i].name); 
            printf("Medication Price: %.2f\n", meds[i].price); 
            printf("Medication Quantity: %d\n", meds[i].quantity); 
            return; 
        } 
    } 
    printf("Medication not found.\n"); 
} 
 
void updateQuantity(int id, int newQty) { 
    for (int i = 0; i < numMeds; i++) { 
        if (meds[i].id == id) { 
            meds[i].quantity = newQty; 
            printf("Quantity updated successfully.\n"); 
            return; 
        } 
    } 
    printf("Medication not found.\n"); 
- 6 -  
} 
 
void deleteMedication(int id) { 
    for (int i = 0; i < numMeds; i++) { 
        if (meds[i].id == id) { 
            for (int j = i; j < numMeds - 1; j++) { 
                meds[j] = meds[j + 1]; 
            } 
            numMeds--; 
            printf("Medication deleted successfully.\n"); 
            return; 
        } 
    } 
    printf("Medication not found.\n"); 
} 
 
void displayMedications() { 
    for (int i = 0; i < numMeds; i++) { 
        printf("Medication ID: %d\n", meds[i].id); 
        printf("Medication Name: %s\n", meds[i].name); 
        printf("Medication Price: %.2f\n", meds[i].price); 
        printf("Medication Quantity: %d\n", meds[i].quantity); 
        printf("--------------------\n"); 
    } 
} 
 
int main() { 
    int choice; 
    int id, newQty; 
 
    do { 
        printf("Pharmacy Management System\n"); 
        printf("1. Add Medication\n"); 
        printf("2. Search Medication\n"); 
        printf("3. Update Medication Quantity\n"); 
        printf("4. Delete Medication\n"); 
        printf("5. Display All Medications\n"); 
        printf("0. Exit\n"); 
        printf("Enter your choice: "); 
        scanf("%d", &choice); 
 
        switch (choice) { 
            case 1: 
                addMedication(); 
                break; 
            case 2: 
                printf("Enter medication ID to search: "); 
                scanf("%d", &id); 
                searchMedication(id); 
                break; 
            case 3: 
- 7 -  
                printf("Enter medication ID to update quantity: "); 
                scanf("%d", &id); 
                printf("Enter new quantity: "); 
                scanf("%d", &newQty); 
                updateQuantity(id, newQty); 
                break; 
            case 4: 
                printf("Enter medication ID to delete: "); 
                scanf("%d", &id); 
                deleteMedication(id); 
                break; 
            case 5: 
                displayMedications(); 
                break; 
            case 0: 
                printf("Exiting...\n"); 
                break; 
            default: 
                printf("Invalid choice. Please try again.\n"); 
        } 
    } while (choice != 0); 
 
    return 0; 
} 
