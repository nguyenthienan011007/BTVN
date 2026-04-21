#23.2
from geopy.distance import distance
import folium
from geopy.geocoders import Nominatim
from geopy.distance import geodesic
geolocator = Nominatim(user_agent="my app")
l1 = geolocator.geocode("UEH University, Ho Chi Minh City")
l2 = geolocator.geocode("Bệnh viện Nhi đồng 1")
l3 = geolocator.geocode("Trường Đại học Bách khoa - Đại học Quốc gia TP.HCM")
l4 = geolocator.geocode("Trung Tâm Thương Mại Vạn Hạnh")
l5 = geolocator.geocode("Bệnh viện Nhân Dân 115")
l6 = geolocator.geocode("Bệnh viện Da Liễu TP.HCM")
l7 = geolocator.geocode("Hội trường Thành uỷ")
l8 = geolocator.geocode("Hotel Nikko Saigon")
l9 = geolocator.geocode("Chợ hoa Hồ Thị Kỷ")
l10 = geolocator.geocode("Bệnh viện Chợ Rẫy")
print(f"Ten:{l1.address}")
print(f"Toa do:{l1.latitude}, {l1.longitude}")
print(f"Ten:{l2.address}")
print(f"Toa do:{l2.latitude}, {l2.longitude}")
print(f"Ten:{l3.address}")
print(f"Toa do:{l3.latitude}, {l3.longitude}")
print(f"Ten:{l4.address}")
print(f"Toa do:{l4.latitude}, {l4.longitude}")
print(f"Ten:{l5.address}")
print(f"Toa do:{l5.latitude}, {l5.longitude}")
print(f"Ten:{l6.address}")
print(f"Toa do:{l6.latitude}, {l6.longitude}")
print(f"Ten:{l7.address}")
print(f"Toa do:{l7.latitude}, {l7.longitude}")
print(f"Ten:{l8.address}")
print(f"Toa do:{l8.latitude}, {l8.longitude}")
print(f"Ten:{l9.address}")
print(f"Toa do:{l9.latitude}, {l9.longitude}")
print(f"Ten:{l10.address}")
print(f"Toa do:{l10.latitude}, {l10.longitude}")
l11 = (l1.latitude,l1.longitude)
d1= distance(Trungtam, l11).km
l12 = (l2.latitude,l2.longitude)
d2= distance(Trungtam, l12).km
l13 = (l3.latitude,l3.longitude)
d3= distance(Trungtam, l13).km
l14 = (l4.latitude,l4.longitude)
d4 = distance(Trungtam, l14).km
l15 = (l5.latitude,l5.longitude)
d5= distance(Trungtam, l15).km
l16 = (l6.latitude,l6.longitude)
d6= distance(Trungtam, l16).km
l17 = (l7.latitude,l7.longitude)
d7= distance(Trungtam, l17).km
l18 = (l8.latitude,l8.longitude)
d8= distance(Trungtam, l18).km
l19 = (l9.latitude,l9.longitude)
d9= distance(Trungtam, l19).km
l110 = (l10.latitude,l10.longitude)
d10= distance(Trungtam, l110).km


Trungtam=[10.773245903507496, 106.6779155566641]
m=folium.Map(location=Trungtam, zoom_start=16)
folium.Marker(Trungtam, popup="UEH cơ sở C",icon=folium.Icon(color='red', icon='star')).add_to(m)
folium.Marker(l11,popup=f"{l1} và cách {d1:.2f} km").add_to(m)
folium.Marker(l12,popup=f"{l2} và cách {d2:.2f} km").add_to(m)
folium.Marker(l13,popup=f"{l3} và cách {d3:.2f} km").add_to(m)
folium.Marker(l14,popup=f"{l4} và cách {d4:.2f} km").add_to(m)
folium.Marker(l15,popup=f"{l5} và cách {d5:.2f} km").add_to(m)
folium.Marker(l16,popup=f"{l6} và cách {d6:.2f} km").add_to(m)
folium.Marker(l17,popup=f"{l7} và cách {d7:.2f} km").add_to(m)
folium.Marker(l18,popup=f"{l8} và cách {d8:.2f} km").add_to(m)
folium.Marker(l19,popup=f"{l9} và cách {d9:.2f} km").add_to(m)
folium.Marker(l110,popup=f"{l10} và cách {d10:.2f} km").add_to(m)

folium.PolyLine(locations=[Trungtam,l11],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l12],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l13],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l14],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l15],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l16],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l17],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l18],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l19],color="red",weight=3).add_to(m)
folium.PolyLine(locations=[Trungtam,l110],color="red",weight=3).add_to(m)








m
