---
layout: post
title: Conception et Implémentation d'un Réseau de Gestion Hôtelière avec Packet Tracer
---

# Conception et Implémentation d'un Réseau de Gestion Hôtelière avec Packet Tracer

## Introduction au Projet
Ce projet détaille la conception et l'implémentation d'un réseau de gestion hôtelière en utilisant Cisco Packet Tracer.  
L'objectif est de créer une infrastructure réseau robuste et sécurisée, capable de supporter les opérations quotidiennes d'un hôtel moderne, incluant la gestion des différents départements (RH, Finance, IT, Accueil, Urgence, Infirmerie) et la connectivité inter-réseaux.  
Nous aborderons les concepts clés tels que les VLANs, le routage inter-VLAN (Router-on-a-Stick), la configuration DHCP, et la connectivité entre routeurs.

## Plan du Projet
Le projet sera structuré en plusieurs phases, couvrant la configuration des équipements réseau et l'implémentation des services essentiels.

### Étape 1 : Configuration Initiale des Routeurs et Switches
Cette étape couvre la configuration de base des interfaces des routeurs et des switches, ainsi que la mise en place des VLANs nécessaires pour segmenter le réseau de l'hôtel.

#### Configuration des Interfaces des Routeurs
```bash
Router>enable
Router#configure terminal
Router(config)#interface Serial0/3/0
Router(config-if)#exit
Router(config)#interface Serial0/3/1
Router(config-if)#exit
Router(config)#interface GigabitEthernet0/1
Router(config-if)#exit
Router(config)#interface GigabitEthernet0/0
Router(config-if)#exit
Router(config)#interface GigabitEthernet0/2
Router(config-if)#exit
Router(config)#interface Serial0/3/0
Router(config-if)#exit
Router(config)#interface Serial0/3/1
Router(config-if)#exit
Router(config)#interface GigabitEthernet0/0
Router(config-if)#no shutdown
Router(config-if)#exit
Router(config)#interface Serial0/3/1
Router(config-if)#clock rate 64000
Router(config-if)#exit
Router(config)#interface Serial0/3/0
Router(config-if)#clock rate 64000
Router(config-if)#exit
Router(config)#do wr