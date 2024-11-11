<template>
  <div class="w-1/3">
    <Card>
      <CardHeader>
        <CardTitle>Neuer Einsatz</CardTitle>
        <CardDescription>Erstelle einen neuen Einsatz</CardDescription>
      </CardHeader>
      <CardContent>
        <div>
          <h4 class="scroll-m-20 text-xl font-semibold tracking-tight">
            Mitteiler
          </h4>
          <div class="flex flex-row gap-4 pt-4">
            <Input placeholder="Name"></Input>
            <Input placeholder="Telefonnummer"></Input>
          </div>
          <div class="flex flex-row gap-4 pt-4">
            <Input placeholder="Zielzeit"></Input>
            <Input placeholder="Erinnerung"></Input>
          </div>
          <h4 class="pt-4 scroll-m-20 text-xl font-semibold tracking-tight">
            Einsatzort
          </h4>
          <div class="pt-4">
            <Input placeholder="Objekt"></Input>
          </div>
          <div class="flex flex-row gap-4 pt-4">
            <Input placeholder="Straße"></Input>
            <Input placeholder="Hausnummer" class="w-1/4"></Input>
          </div>
          <div class="flex flex-row gap-4 pt-4">
            <Input class="w-1/4" placeholder="PLZ"></Input>
            <Input class="" placeholder="Stadt"></Input>
          </div>
          <h4 class="pt-4 scroll-m-20 text-xl font-semibold tracking-tight">
            Ereignis
          </h4>
          <div class="gap-4 pt-4">
            <Input placeholder="Meldebild"></Input>
          </div>
          <div class="flex flex-row gap-4 pt-4">
            <Input placeholder="STW R"></Input>
            <Input placeholder="STW FW"></Input>
            <Button variant="destructive">Autosplit</Button>
          </div>
          <div class="pt-4">
            <Textarea placeholder="Bemerkung"></Textarea>
          </div>
          <h4 class="pt-4 scroll-m-20 text-xl font-semibold tracking-tight">
            Zielort
          </h4>
          <div class="pt-4">
            <Input placeholder="Objekt"></Input>
          </div>
          <div class="flex flex-row gap-4 pt-4">
            <Input placeholder="Straße"></Input>
            <Input placeholder="Hausnummer" class="w-1/4"></Input>
          </div>
          <div class="flex flex-row gap-4 pt-4">
            <Input class="w-1/4" placeholder="PLZ"></Input>
            <Input class="" placeholder="Stadt"></Input>
          </div>
        </div>
        <div class="flex flex-row gap-4 pt-4 justify-end">
          <Button>Speichern (F11)</Button>
          <Button variant="destructive">Disponieren</Button>
        </div>
        <div class="flex flex-row gap-4 pt-4 justify-end">
          <Button variant="secondary">An ELP senden</Button>
          <Button variant="secondary">Wiedereröffnen</Button>
          <Button variant="secondary">Abschließen</Button>
        </div>
      </CardContent>
      <CardFooter>
      </CardFooter>
    </Card>
  </div>
</template>

<script lang="ts" setup>
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle
} from '@/components/ui/card';

import { Input } from '@/components/ui/input';
import { Label } from '@/components/ui/label';
import { Button } from '@/components/ui/button';
import { Textarea } from '@/components/ui/textarea';
</script>

<style></style>