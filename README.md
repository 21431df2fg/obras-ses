# obras-ses// No script, adicione:
function initMap() {
    const map = new google.maps.Map(document.querySelector(".map-container"), {
        zoom: 15,
        center: { lat: -19.9517, lng: -43.9318 } // Coordenadas do Jardim do Vale
    });
    
    // Adicionar marcadores para cada trecho
    sections.forEach(section => {
        new google.maps.Marker({
            position: { lat: section.lat, lng: section.lng },
            map: map,
            title: `Trecho ${section.id} - ${section.name}`
        });
    });
}
