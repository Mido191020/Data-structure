#include <iostream>
using namespace std;

struct node{
    int data;
    node* next;
    node(int data) : data(data) {}
};

class linkedList {
private:
    node* head, * last;
    int length;
public:
    linkedList() : head(NULL), last(NULL), length(0) {}

    void insert_first(int value) {
        node* temp = new node(value);
        temp->next = NULL;
        if (head == NULL) {
            head = last = temp;
            temp = NULL;
        }
        else {
            temp->next = head;
            head = temp;
        }
        length++;
    }

    void insert_end(int value) {
        node* temp = new node(value);
        temp->next = NULL;
        if (head == NULL) {
            head = last = temp;
            temp = NULL;
        }
        else {
            last->next = temp;
            last = temp;
        }
    }

    void delete_first() {
        if (head == NULL) {
            cout << "the list is empty\n";
        }
        else {
            node* temp = head;
            head = head->next;
            delete temp;
        }
    }

    void delete_end() {
        if (head == NULL) return;

        if (head->next == NULL) {
            delete head;
            head = NULL;
            last = NULL;
            return;
        }

        node* temp = head;
        while (temp->next->next != NULL) {
            temp = temp->next;
        }
        delete last;
        last = temp;
        last->next = NULL;
    }

    void print() {
        for (node* next = head; next != NULL; next = next->next) {
            cout << next->data << " ";
        }
        cout << endl;
    }
};

void test_end() {
    linkedList l;
    l.insert_end(10);
    l.insert_end(20);
    l.insert_end(50);
    l.insert_end(30);
    l.print();
    l.delete_end();
    l.print();
}

void test_first() {
    linkedList l;
    l.insert_first(10);
    l.insert_first(30);
    l.insert_first(50);
    l.insert_first(80);
    l.print();
    l.delete_first();
    l.delete_first();
    l.print();
}

int main() {
    test_end();
    return 0;
}
