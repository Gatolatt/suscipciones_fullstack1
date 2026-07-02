package com.subscripciones.subscripciones;

import org.junit.jupiter.api.Test;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.autoconfigure.web.servlet.AutoConfigureMockMvc;
import org.springframework.boot.test.context.SpringBootTest;
import org.springframework.http.MediaType;
import org.springframework.test.web.servlet.MockMvc;

// Importaciones estáticas necesarias para las validaciones del test
import static org.springframework.test.web.servlet.request.MockMvcRequestBuilders.get;
import static org.springframework.test.web.servlet.result.MockMvcResultMatchers.status;
import static org.springframework.test.web.servlet.result.MockMvcResultMatchers.content;

@SpringBootTest
@AutoConfigureMockMvc // Configura MockMvc de forma automática para simular peticiones HTTP
class SubscripcionesApplicationTests {

    @Autowired
    private MockMvc mockMvc;

    @Test
    void debeListarSuscripcionesExitosamente() throws Exception {
        // Simulamos una petición GET a tu endpoint
        mockMvc.perform(get("/api/suscripciones")
                .contentType(MediaType.APPLICATION_JSON))
                // 1. Verificamos que el servidor responda con un Status 200 OK
                .andExpect(status().isOk())
                // 2. Verificamos que el cuerpo del texto sea exactamente el que retorna tu controlador
                .andExpect(content().string("Lista de suscripciones"));
    }
}
