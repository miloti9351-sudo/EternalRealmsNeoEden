# EternalRealmsNeoEden
{
  "name": "eternal-realms-neoeden",
  "version": "0.1.0",
  "private": true,
  "main": "expo-router/entry",
  "scripts": {
    "start": "expo start",
    "android": "expo run:android"
  },
  "dependencies": {
    "expo": "~53.0.0",
    "expo-router": "^4.0.0",
    "react": "18.3.1",
    "react-native": "0.76.0"
  }
}
import { useState } from "react";
import { View, Text, Pressable } from "react-native";

export default function Juego() {
  const [vida, setVida] = useState(100);
  const [xp, setXp] = useState(0);
  const [titanio, setTitanio] = useState(0);

  const explorar = () => {
    setTitanio(titanio + 1);
    setXp(xp + 5);
  };

  const atacar = () => {
    setXp(xp + 10);
  };

  return (
    <View
      style={{
        flex: 1,
        backgroundColor: "#101020",
        justifyContent: "center",
        alignItems: "center"
      }}
    >
      <Text style={{ color: "white", fontSize: 24 }}>
        Neo-Eden
      </Text>

      <Text style={{ color: "#00FFFF" }}>
        Vida: {vida}
      </Text>

      <Text style={{ color: "#FFFF00" }}>
        XP: {xp}
      </Text>

      <Text style={{ color: "#00FF00" }}>
        Titanio: {titanio}
      </Text>

      <Pressable
        onPress={explorar}
        style={{
          backgroundColor: "blue",
          padding: 12,
          borderRadius: 10,
          marginTop: 15
        }}
      >
        <Text style={{ color: "white" }}>
          Explorar
        </Text>
      </Pressable>

      <Pressable
        onPress={atacar}
        style={{
          backgroundColor: "red",
          padding: 12,
          borderRadius: 10,
          marginTop: 15
        }}
      >
        <Text style={{ color: "white" }}>
          Atacar Dron
        </Text>
      </Pressable>
    </View>
  );
}
export interface Player {
  nombre: string;
  nivel: number;
  vida: number;
  experiencia: number;
  monedas: number;
}
export const resources = [
  {
    id: 1,
    nombre: "Titanio"
  },
  {
    id: 2,
    nombre: "Nanocircuitos"
  },
  {
    id: 3,
    nombre: "Cristales Cuánticos"
  }
];
export class Inventory {

  items: string[] = [];

  agregar(item: string) {
    this.items.push(item);
  }

  listar() {
    return this.items;
  }

}
