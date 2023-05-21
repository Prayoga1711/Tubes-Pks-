/* Prayoga Nofriyansyah_122130042_Teknik Elektro
   Endy Tupala_122130041_Teknik Elektro
   Muhammmad Al Fathi_122130040_Teknik Elektro
   
   HUKUM FARADAYY 1
   Program perhitungan hukum faraday 1.
   pada program ini kami mengimplemenstasikan perhitungan hukum faraday 1 dalam c++
   yang dimana kita dapat mencari muatan listrik(Q), arus listrik(i), dan waktu(t) dengan rumus yang 
   sudah diketahui, dapat kita lihat di bawah.*/
   
#include <iostream>
using namespace std ;

int main() {
    cout << "~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~" <<endl;
	cout << "IIIIIIIIII HUKUM FARADAY 1 IIIIIIIIII"<<endl;
	cout << "~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~" <<endl;
	cout << "Hukum Faraday 1 berbunyi: Massa zat yang dihasilkan pada suatu electroda "<<endl;
	cout << "Selama proses elektrolisis berbanding lurus dengan muatan listrik yang digunakan "<<endl;
	int a,b,c;
	
	char ulang= 'y';
    
    while (ulang == 'y' || ulang == 'Y'){
        cout << "Apa yang ingin anda cari?"<<endl;
	    cout << "> Muatan(Q)  (ketik 1)" <<endl;
	    cout << "> Arus listrik(i)  (ketik 2)"<<endl;
	    cout << "> Waktu(t)  (ketik 3)" << endl;
    	cin >> a;
	if (a == 1){
		cout << "Untuk berapa percobaan?"<<endl;
		cin >> b;
		double q[b], i[b], t[b];
		
		for (c=0 ; c<= b-1; c++){
			cout << "Masukkan nilai i " << c + 1 <<endl;
			cin >> i[c];
			cout << "Masukkan nilai t " << c + 1 <<endl;
			cin >> t[c];
			q[c] = i[c] * t[c];		
		}
		for (c=0 ; c<= b-1; c++){
			cout << "Maka nilai dari muatan Q"<< c + 1<< " adalah = " << q[c] << " coulomb " <<endl;
		}			
	} else {
	    	if (a == 2){
		    cout << "Untuk berapa percobaan?"<<endl;
		    cin >> b;
			double q[b], i[b], t[b];
			
			for (c=0 ; c<= b-1; c++){
			    cout << "Masukkan nilai Q " << c + 1 <<endl;
			    cin >> q[c];
			    cout << "Masukkan nilai t " << c + 1 <<endl;
			    cin >> t[c];
			    i[c] = q[c] / t[c];		
			}
			for (c=0 ; c<= b-1; c++){
			    cout << "Maka nilai dari muatan i"<< c + 1<< " adalah = " << i[c] << "ampere" <<endl;
			}
		} else {
		    if (a == 3){
		        cout << "Untuk berapa percobaan?"<<endl;
		        cin >> b;
		        double q[b], i[b], t[b];
		        
		        for (c=0 ; c<= b-1; c++){
		            cout << "Masukkan nilai Q " << c + 1 <<endl;
		            cin >> q[c];
		            cout << "Masukkan nilai i " << c + 1 <<endl;
		            cin >> i[c];
		            t[c] = q[c] / i[c];	
		        }
		        for (c=0 ; c<= b-1; c++){
		            cout << "Maka nilai dari muatan t"<< c + 1<< " adalah = " << t[c] << "detik/sekon"<<endl;
		        }
		    } else {
		        cout << " Eror " <<endl;
		    }
		}
	}
	cout << " > Apakah Anda ingin mengulang program? (y/n): " ;
        cin >> ulang;
    }
    cout << " Terima kasih telah menggunakan program ini :) " <<endl;
}
