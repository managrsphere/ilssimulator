<template>
  <div>
    <Card>
      <CardHeader>
        <CardTitle>Einsatzmittel</CardTitle>
        <CardDescription>Einsatzmittel für den aktuellen Einsatz</CardDescription>
      </CardHeader>
      <CardContent>
        <Input class="w-1/2" placeholder="Einsatzmittel hinzufügen"></Input>
        <div class="pt-4">
          <Table>
            <TableCaption>Vorschlag</TableCaption>
            <TableHeader>
              <TableRow>
                <TableHead class="w-1/3">Funkrufname</TableHead>
                <TableHead class="w-[100px]">Status</TableHead>
                <TableHead class="w-[100px]">Entfernung</TableHead>
                <TableHead class="w-[100px]">Entfernung Luftlinie</TableHead>
              </TableRow>
            </TableHeader>
            <TableBody>
              <TableRow>
                <TableCell class="font-medium">
                  Rotkreuz Regensburg 21/12/2
                </TableCell>
                <TableCell>2</TableCell>
                <TableCell>1,4km</TableCell>
                <TableCell>900m</TableCell>
              </TableRow>
            </TableBody>
          </Table>
        </div>
        <div class="flex flex-row pt-4 justify-end">
          <Button variant="destructive">Alarmieren</Button>
        </div>
        <div class="pt-4">
          <Table>
            <TableCaption>Alle Einsatzmittel im aktuellen Einsatz</TableCaption>
            <TableHeader>
              <TableRow>
                <TableHead class="w-1/3">Funkrufname</TableHead>
                <TableHead class="w-[100px]">Status</TableHead>
                <TableHead class="w-[100px]">S3</TableHead>
                <TableHead class="w-[100px]">S4</TableHead>
                <TableHead class="w-[100px]">S7</TableHead>
                <TableHead class="w-[100px]">S8</TableHead>
                <TableHead class="w-[100px]">S1</TableHead>
                <TableHead class="w-[100px]">S2</TableHead>
              </TableRow>
            </TableHeader>
            <TableBody>
              <TableRow>
                <TableCell class="font-medium">
                  Rotkreuz Regensburg 8/1
                </TableCell>
                <TableCell>4</TableCell>
                <TableCell>12:30</TableCell>
                <TableCell>12:38</TableCell>
                <TableCell>13:04</TableCell>
                <TableCell>13:20</TableCell>
                <TableCell>13:44</TableCell>
                <TableCell>14:02</TableCell>
              </TableRow>
            </TableBody>
          </Table>
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
  CardTitle,
} from '@/components/ui/card'

import {
  Table,
  TableBody,
  TableCaption,
  TableCell,
  TableHead,
  TableHeader,
  TableRow,
} from '@/components/ui/table'

import { Input } from '@/components/ui/input';
import { Button } from '@/components/ui/button';
</script>

<style></style>