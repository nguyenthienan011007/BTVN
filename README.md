#23.5
import folium
khohang=[10.773271126486994, 106.67764631129579]
m = folium.Map(location=khohang, zoom_start=16)
folium.Marker(khohang, popup="Kho hàng", color="red", icon=folium.Icon(color="red")).add_to(m)
folium.Circle([10.774841542986838, 106.68013540121397],color="green",fill=True, radius= 200, popup="Khu vực giao hàng nhanh cách kho hàng 3km",fill_opacity=0.2).add_to(m)
folium.Circle([10.77811066373044, 106.67230100833257],color="yellow",fill=True, radius=250, popup="Khu vực giao hàng trung bình cách kho hàng 7 km",fill_opacity=0.2).add_to(m)
folium.Circle([10.764330109001872, 106.6671604688634],color="red",fill=True, radius= 350, popup="Khu vực giao hàng chậm cách kho hàng 9km",fill_opacity=0.2).add_to(m)
m

#23.5
import folium
nhakho={
    "Kho thứ nhất": [10.772993904229107, 106.67724557469425],
    "Kho thứ hai": [10.774827814292141, 106.6802281910496],
    "Kho thứ ba": [10.77520724256515, 106.6766662175761]
}
m=folium.Map(location=[10.773457652658673, 106.6774601514226],zoom_start=16)
for name,loc in nhakho.items():
  folium.Marker(loc,popup=name, icon=folium.Icon(color="blue")).add_to(m)
  folium.Circle(loc,radius=200,color="red", fill=True, fill_opacity=0.2).add_to(m)
donhang=[{"diachi": [10.766735284815384, 106.68045341881145], "status":"Thời gian giao nhanh"},
{"diachi": [ 10.76638540479643, 106.66148090345771], "status": "Thời gian giao trung bình"},
{"diachi": [10.753036426494953, 106.66878571449656], "status":"Thời gian giao chậm"}]
for order in donhang:
  color = {"Thời gian giao nhanh":"green", "Thời gian giao trung bình":"gray", "Thời gian giao chậm":"red"}[order["status"]]
  folium.Marker(order["diachi"],popup=order["status"],icon=folium.Icon(color=color)).add_to(m)
