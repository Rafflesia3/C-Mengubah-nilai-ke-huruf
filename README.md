# C-Mengubah-nilai-ke-huruf

    #include<iostream>
    #include<string.h>
    #include<cmath>
    using namespace std;

    float n;
    int ribuan,ratusan,puluhan,satuan,koma,r;
    string bil[10]={"","se","dua ","tiga ","empat ","lima ","enam ","tujuh ","delapan ","sembilan "};
    string k;

    int main(){
    cout << "\t\t Pelita Bangsa \n\n" << endl;
    cout << "=========================================\n" << endl;
    cout << "Nama    : Rafi Alwan Setyawan \nNIM     : 311810325 \nKelas   : TI.18.D7 \n" << endl;
    cout << "=========================================\n" << endl;

    cout<< "\t     Mengubah nilai ke huruf\n" << endl;

    cout<<"masukan bilangan = ";cin>>n;r=n;

    if(n>1000){cout<<"error inputan < 1000";
    }else{
    koma=(floor((n-r)*1000+0.1)/1000)*1000;ratusan=r/100;r=r%100;puluhan=r/10;satuan=r%10;
    if(ratusan){
    k+=bil[ratusan]+"ratus ";
     }
     if(puluhan&&r>=20||r==10){
      k+=bil[puluhan]+"puluh ";
     }
     if(satuan&&puluhan==1){
      bil[1]="se";k+=bil[satuan]+"belas ";
     }else if(satuan){
      bil[1]="satu ";k+=bil[satuan];
     }
     if(koma){
      k+="koma ";
      r=koma;
      puluhan=r/100;puluhan=puluhan%100;ratusan=r/10;ratusan=ratusan%10;
     k+=bil[puluhan]+"puluh ";
     k+=bil[ratusan];
     }
     cout<<"\n"<< n <<" Jadi : "<< k<<endl;

     }
    }
    
Hasil
![img](https://github.com/Rafflesia3/C-Mengubah-nilai-ke-huruf/blob/master/C++%20Mengubah%20nilai%20ke%20huruf.png?raw=true)
