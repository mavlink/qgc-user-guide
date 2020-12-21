# Plan Ekranı - Coğrafi Sınır

Coğrafi Sınırlar, aracınızın içinde uçmasına izin verilen ya da *izin verilmeyen* sanal bölgeler oluşturmanıza olanak sağlar. Ayrıca eğer izin verilen alanın dışına çıkıldığında yaplıacak eylemi de ayarlayabilirsiniz.

![Geofence overview](../../assets/plan/geofence/geofence_overview.jpg)

> **Note** **ArduPilot users:** Coğrafi Sınır sadece Rover 3.6 ve Copter3.7 ve üzeri sürümlerde desteklenir. Ek olarak günlük sürümlerin ya da stabil 3.6 sürümünün (erişilebilir olduğunda) kullanılmasını gerektirir. Eğer bağlanan cihaz tarafından Coğrafi Sınır seçeneği desteklenmiyorsa *QGroundControl* seçeneği göstermeyecektir.

## Coğrafi Sınır Oluşturma

Coğrafi Sınır Oluşturmak için:

1. Plan Ekranı'na gidin
2. Görev Komutları Listesi'nin üstünden *Geofence*'i seçin
    
    ![Select geofence radio button](../../assets/plan/geofence/geofence_select.jpg)

3. **Circular Fence** ya da **Polygon Fence** butonlarına basarak, sırasıyla dairesel ya da çokgen bölgeler ekleyin. Haritaya yeni bir bölge ve butonların altına sınırlarla ilgili yeni bir liste eklenecektir.
    
    > **Tip** Butonlara birden çok kez basarak birden çok bölge oluşturabilirsiniz, böylece karmaşık coğrafi sınırlar oluşturulabilir.

- Dairesel Bölge:
    
    ![Circular Geofence](../../assets/plan/geofence/geofence_circular.jpg)
    
    - Merkezi noktayı kaydırarak bölgeyi haritada hareket ettirin
    - Resize the circle by dragging the map dot on the edge of the circle (or you can change the radius value in the fence panel).

- Polygon region:
    
    ![Polygon Geofence](../../assets/plan/geofence/geofence_polygon.jpg)
    
    - Move the vertices by dragging the filled dots
    - Create new vertices by clicking the "unfilled" dots on the lines between the filled vertices. 
        1. By default new regions are created as *inclusion* zones (vehicles must stay within the region). Change them to exclusion zones (where the vehicle can't travel) by unchecking the associated *Inclusion* checkbox in the fence panel.

## Edit/Delete a GeoFence

You can select a geofence region to edit by selecting its *Edit* radio button in the GeoFence panel. You can then edit the region on the map as described in the previous section.

Regions can be deleted by pressing the associated **Del** button

## Upload a GeoFence

The GeoFence is uploaded in the same way as a mission, using **File** in the [Plan tools](../PlanView/PlanView.md).

## Remaining tools

The rest of the tools work exactly as they do while editing a Mission.