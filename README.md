# EternalRealmsNeoEden
import { View, Text, Pressable } from "react-native";
import { router } from "expo-router";

export default function Home() {
  return (
    <View
      style={{
        flex: 1,
        backgroundColor: "#050510",
        justifyContent: "center",
        alignItems: "center"
      }}
    >
      <Text
        style={{
          color: "#00FFFF",
          fontSize: 32,
          fontWeight: "bold"
        }}
      >
        Eternal Realms
      </Text>

      <Text
        style={{
          color: "#FFFFFF",
          marginBottom: 20
        }}
      >
        Neo-Eden
      </Text>

      <Pressable
        onPress={() => router.push("/juego")}
        style={{
          backgroundColor: "#00FFFF",
          padding: 15,
          borderRadius: 12
        }}
      >
        <Text>Iniciar Juego</Text>
      </Pressable>
    </View>
  );
}
