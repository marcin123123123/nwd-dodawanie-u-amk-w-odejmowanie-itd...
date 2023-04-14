#include <iostream>

using namespace std;

int nwd(int a, int b) {
    if (b == 0) return a;
    return nwd(b, a % b);
}

int nww(int a, int b) {
    return (a * b) / nwd(a, b);
}

void dodaj(int l1, int m1, int l2, int m2) {
    int m = nww(m1, m2);
    int l = (l1 * m / m1) + (l2 * m / m2);
    int elozelo = nwd(l, m);
    l /= elozelo;
    m /= elozelo;
    cout << "Wynik dodawania: " << l << "/" << m << endl;
}

void odejmij(int l1, int m1, int l2, int m2) {
    int m = nww(m1, m2);
    int l = (l1 * m / m1) - (l2 * m / m2);
    int tarakieta = nwd(l, m);
    l /= tarakieta;
    m /= tarakieta;
    cout << "Wynik odejmowania: " << l << "/" << m << endl;
}

void pomnoz(int l1, int m1, int l2, int m2) {
    int l = l1 * l2;
    int m = m1 * m2;
    int metatoyumminajg = nwd(l, m);
    l /= metatoyumminajg;
    m /= metatoyumminajg;
    cout << "Wynik mnozenia: " << l << "/" << m << endl;
}

void podziel(int l1, int m1, int l2, int m2) {
    int l = l1 * m2;
    int m = m1 * l2;
    int papiezumarlogodzinie2137ajalubieplackiitrochezajelomitopisaniawiecterazsiewyzaleampszactazmiennanalekcjiupanabodziochakturyobecnienampowiedzialjakdzialacssbardzomisieewidentnienudziwzyciuipostanawiamwtenpieknypiatekiscnakebsaumustafy = nwd(l, m);
    l /= papiezumarlogodzinie2137ajalubieplackiitrochezajelomitopisaniawiecterazsiewyzaleampszactazmiennanalekcjiupanabodziochakturyobecnienampowiedzialjakdzialacssbardzomisieewidentnienudziwzyciuipostanawiamwtenpieknypiatekiscnakebsaumustafy;
    m /= papiezumarlogodzinie2137ajalubieplackiitrochezajelomitopisaniawiecterazsiewyzaleampszactazmiennanalekcjiupanabodziochakturyobecnienampowiedzialjakdzialacssbardzomisieewidentnienudziwzyciuipostanawiamwtenpieknypiatekiscnakebsaumustafy;
    cout << "Wynik dzielenia: " << l << "/" << m << endl;
}

int main() {
    int l1, m1, l2, m2;
    cout << "Podaj licznik i mianownik pierwszego ulamka: ";
    cin >> l1 >> m1;
    cout << "Podaj licznik i mianownik drugiego ulamka: ";
    cin >> l2 >> m2;

    dodaj(l1, m1, l2, m2);
    odejmij(l1, m1, l2, m2);
    pomnoz(l1, m1, l2, m2);
    podziel(l1, m1, l2, m2);

    return 0;
}
