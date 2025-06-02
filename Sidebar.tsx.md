"use client";

import React from 'react';
import Link from 'next/link';
import {
    LayoutDashboard,
    ListChecks,
    Calendar,
    Settings,
    User,
    Project,
} from 'lucide-react';
import Image from 'next/image';

const Sidebar = () => {
    return (
        <div className="w-64 h-screen bg-gray-800 text-white fixed top-0 left-0 flex flex-col">
            {/* App Logo */}
            <div className="h-16 flex items-center justify-center">
                <Link href="/" className="text-lg font-semibold">TaskFlow</Link>
            </div>

            {/* Navigation Links */}
            <nav className="flex-1 p-4">
                <ul>
                    <li className="mb-2">
                        <Link href="/" className="flex items-center p-2 hover:bg-gray-700 rounded-md">
                            <LayoutDashboard className="mr-2 h-4 w-4" />
                            Dashboard
                        </Link>
                    </li>
                    <li className="mb-2">
                        <Link href="/projects" className="flex items-center p-2 hover:bg-gray-700 rounded-md">
                            <Project className="mr-2 h-4 w-4" />
                            Projects
                        </Link>
                    </li>
                    <li className="mb-2">
                        <Link href="/tasks" className="flex items-center p-2 hover:bg-gray-700 rounded-md">
                            <ListChecks className="mr-2 h-4 w-4" />
                            Tasks
                        </Link>
                    </li>
                    <li className="mb-2">
                        <Link href="/calendar" className="flex items-center p-2 hover:bg-gray-700 rounded-md">
                            <Calendar className="mr-2 h-4 w-4" />
                            Calendar
                        </Link>
                    </li>
                    <li className="mb-2">
                        <Link href="/settings" className="flex items-center p-2 hover:bg-gray-700 rounded-md">
                            <Settings className="mr-2 h-4 w-4" />
                            Settings
                        </Link>
                    </li>
                </ul>
            </nav>

            {/* User Profile */}
            <div className="p-4 border-t border-gray-700">
                <div className="flex items-center">
                    <Image
                        src="https://picsum.photos/40/40" // Replace with actual user avatar
                        alt="User Avatar"
                        width={40}
                        height={40}
                        className="rounded-full mr-2"
                    />
                    <div>
                        <p className="text-sm font-semibold">John Doe</p>
                        <p className="text-xs text-gray-400">Online</p>
                    </div>
                </div>
            </div>
        </div>
    );
};

export default Sidebar;
