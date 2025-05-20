Bu layihə müştəri xidmətlərini təhlil və vizuallaşdırmaq məqsədilə Power BI istifadə edilərək hazırlanmışdır. 
Dashboard vasitəsilə operator performansı, zəng növləri, müştəri məmnuniyyəti və riskli nöqtələr kimi göstəricilər interaktiv şəkildə təqdim olunur.
 
 Əsas Xüsusiyyətlər
Operatorlar üzrə zəng sayı və performans təhlili
Zəng səbəblərinə (şikayət, məlumat, dəstək və s.) görə təsnifat
Müştəri məmnuniyyəti üzrə reyting
Loyal müştərilərin təyin edilməsi
Zaman üzrə müraciət trendi və sıxlıq analizi
Dinamik filtrlər və slicerlərlə interaktiv analiz imkanı

  İstifadə Edilən DAX Formulları:
	Evvelki Ay = 
CALCULATE(
    COUNT(Calls[Zeng_ID]),
    PREVIOUSMONTH('CalendarAuto'[Date]))

	Mobil Operator = 
SWITCH(
    MID(Calls[Mobil_nomre],4,2),"50","Azercell","51","Azercell","55","Bakcell","Nar")


Müşteri Ad,Soyadi,Ata adi = 
    CONCATENATE(Customers[Ad],
    CONCATENATE(" ",
    CONCATENATE(Customers[Soyad],
    CONCATENATE(" ",Customers[Ata_adi]))))

Dashboard əsaslanaraq zəng sıxlığını nəzərə alaraq qrafiklərin uyğunlaşdırılmasını
KPİ ların təyin edilməsini
Zəng səbəblərinə əsasən riskli və ya problemli nöqtələrin təyin edilməsini tövsiyyə edə bilərik
 
