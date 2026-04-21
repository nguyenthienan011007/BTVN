#23.1
import folium
UEH = [10.77335544435826, 106.67756048060969]
BV = [10.775326367872198, 106.68137994614148]
TTTM = [10.770815358110555, 106.66987863423174]
HV = [10.773610721650776, 106.677037708153581]
TTTM2 = [10.776246273168042, 106.68092064110766]
m=folium.Map(location=[10.77335544435826, 106.67756048060969],zoom_start=16)
folium.Marker(UEH, popup = " Đại học Kinh tế Tp HCM ").add_to(m)
folium.Marker(BV, popup ="Bệnh viện Bình Dân - Khu điều trị Kỹ thuật cao").add_to(m)
folium.Marker(TTTM, popup ="Trung Tâm Thương Mại Vạn Hạnh").add_to(m)
folium.Marker(HV, popup ="Phân hiệu Học viện Hành chính và Quản trị công tại Thành phố Hồ Chí Minh").add_to(m)
folium.Marker(TTTM2, popup ="Vincom Plaza 3/2").add_to(m)


m
