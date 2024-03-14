# Gerar-Terreno-Aleat-rio-em-Unity-
Script para Gerar Terreno Aleatório em Unity

using UnityEngine;

public class RandomTerrainGenerator : MonoBehaviour
{
    public GameObject terrainPrefab;
    public int terrainWidth = 10;
    public int terrainHeight = 10;

    void Start()
    {
        GenerateTerrain();
    }

    void GenerateTerrain()
    {
        for (int x = 0; x < terrainWidth; x++)
        {
            for (int y = 0; y < terrainHeight; y++)
            {
                Vector3 position = new Vector3(x, 0f, y);
                Instantiate(terrainPrefab, position, Quaternion.identity);
            }
        }
    }
}
